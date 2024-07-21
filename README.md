# 📊 [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

_Amazon SageMaker Canvas é uma ferramenta de machine learning sem código oferecida pela AWS. Ele permite que usuários, mesmo sem experiência em programação, construam, treinem e implantem modelos de machine learning. Utilizando uma interface intuitiva, o SageMaker Canvas facilita a criação de previsões e insights a partir de dados empresariais, acelerando o processo de tomada de decisão._

## 📋 Descrição do Projeto

Previsão de Estoque Inteligente na AWS com SageMaker Canvas

Neste projeto, intitulado "Previsão de Estoque Inteligente na AWS com SageMaker Canvas", aprendi a utilizar o SageMaker Canvas para integrar e gerenciar o estoque de forma inteligente, baseada em machine learning. Seguindo o passo a passo do Lab DIO, construí modelos preditivos que ajudaram a otimizar o controle de inventário, melhorando a eficiência operacional e reduzindo custos.


## 🎯 Objetivos Deste Desafio de Projeto (Lab)

![image](https://github.com/digitalinnovationone/lab-aws-sagemaker-canvas-estoque/assets/730492/72f5c21f-5562-491e-aa42-2885a3184650)

O principal objetivo deste desafio de projeto foi desenvolver habilidades práticas e aplicar conhecimentos na área de previsão de estoque de produtos utilizando o AWS SageMaker Canvas.


## 🚀 Passo a Passo

### 1. Selecionar Dataset

-   Escolha do dataset na pasta `datasets` deste repositório.

[Dataset selecionado para criar o modelo](https://github.com/emanoellavaldevino/lab-aws-sagemaker-canvas-estoque/blob/main/datasets/dataset-1000-com-preco-variavel-e-renovacao-estoque.csv)

####

-   Upload do dataset foi feito com sucesso no SageMaker Canvas.

![image](https://github.com/emanoellavaldevino/lab-aws-sagemaker-canvas-estoque/blob/main/Imagem/Amazon_Canvas_1.png)

- Visualização das primeiras 5 linhas do arquivo.

![image](https://github.com/emanoellavaldevino/lab-aws-sagemaker-canvas-estoque/blob/main/Imagem/PreparandoDados2.png)

### 2. Construir/Treinar

-   Configuração das variáveis de entrada e saída de acordo com os dados.

![image](https://github.com/emanoellavaldevino/lab-aws-sagemaker-canvas-estoque/blob/main/Imagem/quantidade_estoque3.png)

- Configuração do modelo.

![image](https://github.com/emanoellavaldevino/lab-aws-sagemaker-canvas-estoque/blob/main/Imagem/CONFIGURACAO_CANVAS4.png)

- Início do treinamento do modelo (isso pode levar algum tempo).

![image](https://github.com/emanoellavaldevino/lab-aws-sagemaker-canvas-estoque/blob/main/Imagem/ANALYSE_5.png)


### 3. Analisar

Após o treinamento, as métricas de performance do modelo foram as seguintes:

![image](https://github.com/emanoellavaldevino/lab-aws-sagemaker-canvas-estoque/blob/main/Imagem/ANALYSE_6.png)


### **Interpretação das Métricas**

Para avaliar o desempenho de um modelo, é essencial analisar diversas métricas. **Valores mais baixos de Avg. wQL, MAPE, WAPE, RMSE e MASE indicam um desempenho superior do modelo, pois refletem menores erros em relação aos dados reais.** Cada métrica fornece uma perspectiva única sobre a precisão do modelo, sendo fundamental considerar várias delas para obter uma visão abrangente e detalhada do desempenho.

**Avg. wQL (Average weighted Quantile Loss)**

Função: Mede a diferença entre os valores previstos e os valores reais em diferentes quantis da distribuição dos dados. É útil para avaliar a precisão de previsões em cenários onde se deseja entender o desempenho do modelo em diferentes pontos da distribuição dos dados.

Interpretação: Quanto menor o valor do Avg. wQL, melhor é o desempenho do modelo, indicando previsões mais precisas em diversos quantis.

**MAPE (Mean Absolute Percentage Error)**

Função: Calcula a média das diferenças absolutas entre os valores previstos e os valores reais, expressa em termos percentuais. É uma métrica que permite entender o erro em relação ao tamanho dos valores reais.

Interpretação: Quanto menor o valor do MAPE, melhor, pois indica que os erros das previsões são pequenos em relação aos valores reais.

**WAPE (Weighted Absolute Percentage Error)**

Função: Similar ao MAPE, mas leva em consideração a soma ponderada das diferenças absolutas entre os valores previstos e reais. É útil quando há diferentes pesos ou importâncias associadas a diferentes dados.

Interpretação: Valores menores de WAPE indicam melhores previsões, considerando as ponderações atribuídas aos dados.

**RMSE (Root Mean Squared Error)**

Função: Mede a raiz quadrada da média dos quadrados das diferenças entre os valores previstos e os valores reais. Penaliza erros maiores mais severamente devido à elevação ao quadrado.

Interpretação: Quanto menor o valor do RMSE, melhor, pois indica que as previsões do modelo estão próximas dos valores reais, com menor variação de erro.

**MASE (Mean Absolute Scaled Error)**

Função: Calcula a média dos erros absolutos escalados pela média dos erros absolutos de um modelo de referência (como o modelo de previsão ingênuo). É uma métrica independente da escala dos dados.

Interpretação: Um valor de MASE menor que 1 indica que o modelo está performando melhor que o modelo de referência. Quanto menor o valor do MASE, melhor é o desempenho do modelo.


### 4. Prever

- O modelo foi treinado com os dados de vários produtos contidos na planilha e foi utilizado para fazer previsões de estoque em produtos específicos. E escolhi uma para dar o exemplo, o modelo do SageMaker Canvas trouxe como resultado os parametros **"p10, p50 e p90"**.
  
![image](https://github.com/emanoellavaldevino/lab-aws-sagemaker-canvas-estoque/blob/main/Imagem/PREDICT_7.png)


**P10 (Percentil 10)** 

Indica que 10% das previsões de estoque são iguais ou menores que esse valor. Em outras palavras, é o valor abaixo do qual está o 10º percentil das previsões de estoque. Pode ser interpretado como uma estimativa conservadora ou pessimista para o estoque.


**P50 (Percentil 50 ou Mediana)**

Representa o valor no qual metade das previsões de estoque são menores e metade são maiores. É uma medida de tendência central e indica o valor central das previsões de estoque.


**P90 (Percentil 90)**

Indica que 90% das previsões de estoque são iguais ou menores que esse valor. É uma estimativa que captura um nível mais otimista ou expansivo para o estoque.

## 📚 Conclusão

O projeto "Previsão de Estoque Inteligente na AWS com SageMaker Canvas" demonstrou com sucesso a aplicação de técnicas de machine learning para otimizar a gestão de inventário. Utilizando o SageMaker Canvas, foi possível construir, treinar e avaliar modelos preditivos sem a necessidade de codificação, tornando a tecnologia acessível mesmo para aqueles sem experiência em programação.

### Principais Aprendizados:

- Facilidade de Uso do SageMaker Canvas: A interface intuitiva permitiu a manipulação e análise de dados de forma eficiente, facilitando a construção de modelos preditivos.
- Eficiência na Gestão de Estoque: A aplicação de modelos preditivos ajudou a prever com precisão a demanda de produtos, contribuindo para a redução de custos operacionais e melhoria da eficiência.
- Análise de Métricas de Performance: A análise das métricas Avg. wQL, MAPE, WAPE, RMSE e MASE forneceu uma compreensão abrangente do desempenho do modelo, permitindo ajustes e melhorias contínuas.

Em resumo, este projeto destacou o potencial do machine learning para transformar a gestão de estoque, tornando-a mais eficiente e estratégica. A experiência adquirida e as ferramentas utilizadas abriram novas possibilidades para futuras implementações e aprimoramentos.


By **Emanoella Valdevino**
