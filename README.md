# Predição de Churn em empresas de telecomunicações

**Autor:** Vitor Pedrique Moura e Silva
**Instituição:** Ilum Escola de Ciência, CNPEM
Disciplina Aprendizado de Máquina, referente ao 2º semestre

## Sobre o Projeto
Este repositório contém um projeto de Machine Learning que foi desenvolvido para prever o cancelamento de serviços (*churn*) por clientes em uma empresa de telecomunicações, utilizando o dataset *Telco Customer Churn*. O objetivo é identificar clientes que tendem a cancelar seus planos, e comparar o desempenho e o custo computacional de 5 algoritmos de classificação: Regressão Logística, KNearestNeighbors, Árvore de Decisão, Floresta Aleatória e XGBoost (além de um Baseline). O desempenho dos modelos será avaliado em ROC-AUC e F1 Score.

## Estrutura do Notebook
O desenvolvimento do projeto está organizado nas seguintes etapas:
**Análise Exploratória e Pré-processamento:** Tratamento de valores ausentes, correção de tipos de dados ("TotalCharges", "SeniorCitizen"), estatísticas descritivas, codificação de variáveis categóricas e normalização.
**Pipeline de Treinamento e Otimização:** Utilização do "ImbPipeline" para evitar vazamento de dados, combinado com **SMOTE** para balanceamento dos dados, **SelectKBest** para seleção de atributos e otimização de hiperparâmetros com **Optuna**, além de validação cruzada estratificada pelo **StratifiedKFold** com folds $k = 5$
**Criação e Treinamento de Modelos** Baseline, Regressão Logística, KNearestNeighbors (KNN), Árvore de Decisão, Floresta Aleatória (Random Forest) e XGBoost.
**Discussão de Resultados e Conclusão:** Comparação das métricas **ROC-AUC** e **F1 Score**, análise das curvas de ROC e discussão do custo benefício entre desempenho dos modelos e custo computacional.
**Interações com AI e Referências:** Esclarecimento quanto ao uso de AI e quanto às referências utilizadas no projeto.

## Principais Resultados
**Desempenho Geral:** Todos os modelos superaram o *baseline*, alcançando pontuações de **ROC-AUC** acima de $0.80$. O **F1 Score** manteve-se abaixo de $0.65$ devido ao desbalanceamento dos dados do dataset (mesmo que a estratégia SMOTE tenha sido utilizada) e à presença de falsos positivos.
**Custo Computacional vs. Eficiência:** Modelos mais complexos (XGBoost e Floresta Aleatória) exigiram alto custo computacional na otimização, enquanto seus desempenhos foram semelhantes aos de modelos mais simples. A **Regressão Logística** destacou-se como uma das melhores relações custo-benefício, atingindo métricas muito semelhantes às dos melhores modelos, enquanto garantia um baixo custo computacional (curto tempo de processamento).

## Como posso executar este projeto?
Baixe os arquivos Tiamat.ipynb e Brasão Tiamat.jpeg, referentes ao notebook Jupyter e a imagem com o brasão recreativo do projeto, respectivamente. 
