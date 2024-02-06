# Solução para Desafio de Projeto

- Esta é a solução para o desafio de Aprendizagem Automatizada utilizando Azure Machine Learning, como parte do Bootcamp **Microsoft Azure AI Fundamentals**

## Passo a passo do processo

- Realizar o cadastro na plataforma Azure: é possível utilizar a versão gratuita, porém é necessário validar um cartão de crédito
- Selecionar o serviço "Azure Machine Learning" na plataforma do Azure
- Criar um novo workspace e, dentro dele, criar um novo "resource group"
- Aguardar a finalização da validação e clicar em criar
- Uma nova tela motra o andamento da implantação até a finalização do deploy
- Clicar em "Ir para recurso" e então em "Iniciar estúdio"
- Escolher o workspace e ir para "ML automatizado" para criar um "new ML automated job"
- Preencher os dados com informações fornecidas pela documentação (nome, tipo de tarefa, tipo de dados)
- Escolher a fonte da dados (web files) e especificar a URL, que passará por uma validação e verificação
- Criar o dataset e selecioná-lo a fim de inserir as informações necessárias
- Submeter o trabalho de treinamento até sua finalização
- É possível acessar as informações do modelo em "Outputs" e o trabalho clicando no link gerado
- Acessar as métricas do trabalho, que trazem dois gráficos (predicted_true e residuals), com informações de valores previstos comparados com os reais
- Retornar ao modelo, escolher a opção de "Deploy Web Service", preencher com as informações da documentação e clicar em "Deploy"
- Após a finalização do deploy, ir para a aba de Endpoints (Pontos de extremidade) para confirmar o status "Succeeded" e ir para a aba "Teste"
- Substituir o json existente pelo código fornecido pela documentação e clicar em "Test"

```
 {
   "Inputs": { 
     "data": [
       {
         "day": 1,
         "mnth": 1,   
         "year": 2022,
         "season": 2,
         "holiday": 0,
         "weekday": 1,
         "workingday": 1,
         "weathersit": 2, 
         "temp": 0.3, 
         "atemp": 0.3,
         "hum": 0.3,
         "windspeed": 0.3 
       }
     ]    
   },   
   "GlobalParameters": 1.0
 }
```

- Resultado do Teste:

```
{
  "Results": [
    331.839379193704
  ]
}
```


