# Relatório do Projeto – Inteligência Artificial

## 1) Título
**Predição de Mortes por Tuberculose Utilizando Aprendizado de Máquina**

## 2) Integrantes
- Tales Hernandes – RA: 10408846 – E-mail: 10408846

## 3) Resumo
Este projeto tem como objetivo aplicar técnicas de Inteligência Artificial para analisar e prever o número estimado de mortes por tuberculose (todas as formas) a cada 100.000 habitantes em diferentes países e períodos históricos. Utilizando dados da Organização Mundial da Saúde (OMS) disponibilizados via Gapminder, serão explorados padrões temporais, regionais e socioeconômicos relacionados à tuberculose, com o intuito de identificar fatores críticos que afetam a mortalidade. Pretende-se aplicar modelos de Machine Learning para criar um sistema preditivo que auxilie no monitoramento e combate da doença.

## 4) Introdução

### a. Contextualização
A tuberculose é uma das doenças infecciosas mais letais do mundo, afetando milhões de pessoas todos os anos. Apesar dos avanços na medicina, ainda representa um grande desafio de saúde pública, especialmente em países de baixa e média renda.

### b. Justificativa
A análise de dados históricos pode auxiliar governos e organizações internacionais a direcionarem políticas públicas e recursos para o combate da tuberculose. O uso de Inteligência Artificial permite identificar padrões e prever cenários futuros, o que pode contribuir para a redução da mortalidade.

### c. Objetivo
- Realizar uma análise exploratória dos dados históricos de mortalidade por tuberculose;  
- Aplicar modelos de Machine Learning (classificação/regressão) para prever a evolução da mortalidade;  
- Avaliar o desempenho dos modelos e interpretar os resultados obtidos.  

### d. Opção do Projeto
**Framework:** utilização do scikit-learn para análise e modelagem preditiva.
 
## 5) Descrição do Problema
Apesar dos esforços da OMS e governos locais, a tuberculose continua a ser uma das principais causas de morte em diversos países. A previsão da mortalidade com base em dados históricos pode auxiliar na tomada de decisão e no direcionamento de recursos. O problema consiste em desenvolver um modelo de aprendizado de máquina capaz de prever a taxa de mortes por tuberculose em diferentes regiões.

## 6) Aspectos Éticos e Responsabilidade
O uso da IA em saúde exige responsabilidade. Modelos preditivos não substituem diagnósticos médicos, mas podem apoiar políticas públicas. É importante garantir que os dados sejam tratados de forma ética, evitando vieses geográficos ou socioeconômicos que possam comprometer a interpretação. Além disso, os resultados devem ser apresentados de forma transparente, sem criar pânico ou interpretações equivocadas.

## 7) Dataset, Análise Exploratória e Preparação dos Dados
O dataset utilizado foi obtido no portal [Gapminder](https://www.gapminder.org/data/), com origem nos dados oficiais da [Organização Mundial da Saúde (WHO)](https://www.who.int/tb/en/). Ele contém o número estimado de mortes por tuberculose (todas as formas) por 100.000 habitantes em diversos países e territórios, no período de 2000 a 2023.

- **Dimensão do dataset:** 214 linhas (países/regiões) e 24 colunas de anos (2000 a 2023), além da coluna de identificação do país.  
- **Análise Exploratória:**
  - Há valores ausentes em alguns anos iniciais (2000–2010), mas a partir de 2011 os dados estão completos.  
  - A média global de mortalidade por tuberculose vem diminuindo desde 2000, embora alguns países, sobretudo na África Subsaariana, apresentem taxas ainda muito elevadas.  
  - Em 2023, os países mais críticos incluem Lesoto, República Centro-Africana e Gabão, com valores superiores a 100 mortes por 100k habitantes.  

- **Preparação dos Dados:**
  - Valores ausentes tratados por meio de imputação pela **média**.  
  - Normalização aplicada via **StandardScaler**, garantindo comparabilidade entre variáveis temporais.  
  - Definição de **variáveis explicativas (X):** anos de 2000 a 2022.  
  - Definição da **variável alvo (y):** ano de 2023.  
  - Divisão em **treino (80%)** e **teste (20%)**, permitindo avaliação justa dos modelos de Machine Learning.  

## 8) Metodologia e Resultados Esperados

### Metodologia
O projeto utilizará técnicas de **Ciência de Dados** e **Aprendizado de Máquina** para prever a taxa estimada de mortes por tuberculose (TB) por 100.000 habitantes em diferentes países. O processo metodológico será estruturado em etapas:

1. **Coleta e Organização dos Dados**
   - Utilização de dataset disponibilizado pela **Organização Mundial da Saúde (WHO)**, contendo estimativas anuais de mortalidade por todas as formas de tuberculose entre 2000 e 2023.

2. **Análise Exploratória dos Dados (EDA)**
   - Identificação de padrões, tendências históricas e diferenças regionais.
   - Verificação de valores ausentes e inconsistências nos registros.
   - Visualização temporal das séries de mortalidade.

3. **Pré-processamento e Preparação dos Dados**
   - Tratamento de valores ausentes por imputação.
   - Normalização das variáveis para garantir melhor desempenho dos modelos.
   - Separação entre variáveis explicativas (anos 2000–2022) e variável alvo (ano 2023).

4. **Modelagem Preditiva**
   - Teste de diferentes algoritmos supervisionados de regressão, incluindo **Regressão Linear, Ridge, Lasso e Random Forest**.
   - Validação cruzada e comparação entre modelos com base em métricas como **R² (coeficiente de determinação), MAE (Erro Absoluto Médio) e RMSE (Raiz do Erro Quadrático Médio)**.

5. **Avaliação e Interpretação dos Resultados**
   - Comparação entre valores reais e previstos para países do conjunto de teste.
   - Análise da acurácia dos modelos e discussão sobre limitações (ex.: variáveis externas não incluídas, como condições socioeconômicas, campanhas de saúde pública e acesso a tratamento).

### Resultados Esperados
- Construção de um modelo capaz de **prever a mortalidade por tuberculose com boa precisão**, utilizando apenas dados históricos de séries temporais.  
- Geração de insights sobre a **evolução da doença em diferentes países**.  
- Contribuição prática para a formulação de políticas públicas de saúde, permitindo a identificação antecipada de regiões com maior risco.  

---

## 9) Referências

- Organização Mundial da Saúde (WHO). *Global Tuberculosis Report 2023*. Disponível em: <https://www.who.int/teams/global-tuberculosis-programme/data>.  
- Géron, A. *Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow*. 2ª ed. O’Reilly Media, 2019.  
- James, G.; Witten, D.; Hastie, T.; Tibshirani, R. *An Introduction to Statistical Learning: with Applications in R*. Springer, 2013.  

---

## 10) Bibliografia

- Alpaydin, E. *Introduction to Machine Learning*. MIT Press, 2020.  
- Kuhn, M.; Johnson, K. *Applied Predictive Modeling*. Springer, 2013.  
- Han, J.; Kamber, M.; Pei, J. *Data Mining: Concepts and Techniques*. Morgan Kaufmann, 2012.  
- WHO. *Tuberculosis Data Portal*. Disponível em: <https://www.who.int/teams/global-tuberculosis-programme/data>.  

