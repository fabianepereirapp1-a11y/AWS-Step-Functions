# AWS-Step-Functions
Este repositório serve como um guia e conjunto de exemplos sobre o AWS Step Functions, um serviço de orquestração serverless que permite aos desenvolvedores criar fluxos de trabalho visuais para coordenar microserviços e outros serviços AWS.
Em vez de escrever código complexo para gerenciar a lógica, tratamento de erros e a sequência de componentes, o Step Functions permite definir tudo isso em um modelo visual e declarativo (JSON/ASL).
Benefícios
1. Orquestração Visual: Permite definir fluxos de trabalho (workflows) arrastando e soltando etapas, facilitando a compreensão do processo
2. Tratamento de Erros:	Lida automaticamente com falhas, tentativas (retries) e tratamento de erros (catch), aumentando a resiliência do aplicativo.
3. Escalabilidade:	Gerencia o estado e a execução em escala, sem a necessidade de provisionar ou gerenciar a infraestrutura subjacente.
4. Integração Nativa:	Integra-se nativamente com mais de 220 serviços AWS, incluindo Lambda, ECS, SQS, SNS, DynamoDB, entre outros.

 Estrutura de Exemplo em ASL (Task State)
O núcleo de qualquer Step Function é a definição do Estado. Abaixo, um exemplo simples de um Task State que invoca uma função Lambda.
{
  "Comment": "Workflow que invoca uma Lambda",
  "StartAt": "Invocar Minha Funcao",
  "States": {
    "Invocar Minha Funcao": {
      "Type": "Task",
      "Resource": "arn:aws:states:::lambda:invoke",
      "Parameters": {
        "FunctionName": "arn:aws:lambda:us-east-1:123456789012:function:MinhaFuncaoLambda"
      },
      "End": true
    }

    Passos:
    1. Criar a Stat Machine usando Console do AWS Step Functions
    2. Definir ASL
    3. Execução
  }
}
