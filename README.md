# Teste de Performance 3: Classificador de Sinais de Sonar (Rocha vs. Mina)

Este repositório contém o terceiro Teste de Performance (TP) do bloco de Machine Learning, focado em classificação binária com técnicas avançadas como Análise de Componentes Principais (PCA) и otimização de hiperparâmetros.

### Objetivo

O projeto visa construir e otimizar um modelo de Machine Learning para classificar objetos subaquáticos como rochas ou minas (cilindros metálicos) com base em seus sinais de sonar.

### Base de Dados

O dataset utilizado é o **"Connectionist Bench (Sonar, Mines vs. Rocks)"**, proveniente do repositório da UCI. Ele contém 208 amostras de sinais de sonar refletidos.
* **Features:** 60 atributos numéricos que representam a energia do sinal de sonar em diferentes frequências.
* **Target:** A classificação do objeto, sendo 'R' para Rocha (Rock) ou 'M' para Mina (Mine).

O dataset pode ser acessado [neste link](https://github.com/professortiagoinfnet/inteligencia_artificial/blob/main/sonar_dataset.csv).

### Etapas do Projeto

1.  **Pré-processamento e Análise de Dados:**
    * Carregamento e inspeção inicial do dataset.
    * Codificação da variável alvo (R/M) para formato numérico.

2.  **Redução de Dimensionalidade com PCA:**
    * Aplicação da **Análise de Componentes Principais (PCA)** para reduzir o número de features (de 60 para um número menor), mantendo a maior parte da variância dos dados. O objetivo é simplificar o modelo e potencialmente melhorar sua performance.

3.  **Treinamento e Otimização do Modelo (Árvore de Decisão):**
    * Desenvolvimento de um modelo de classificação usando **Árvores de Decisão**.
    * Utilização de **GridSearch com Validação Cruzada** para buscar sistematicamente a melhor combinação de hiperparâmetros (ex: `max_depth`, `min_samples_leaf`).
    * Aplicação de **pruning (poda)**, controlada pelos hiperparâmetros encontrados, para evitar overfitting e aumentar a capacidade de generalização do modelo.

4.  **Avaliação de Performance:**
    * Análise detalhada da eficiência do modelo otimizado utilizando um conjunto de teste.
    * As métricas de avaliação incluem:
        * Acurácia (Accuracy)
        * Precisão (Precision)
        * Recall (Sensibilidade)
        * F1-Score
        * Curva ROC (AUC)

5.  **Análise de Resultados e Conclusão:**
    * Interpretação das métricas para avaliar a eficácia do classificador na tarefa de distinguir rochas de minas.
    * Discussão sobre o impacto do PCA e da otimização de hiperparâmetros nos resultados finais.
