# Relatório do Projeto – Inteligência Artificial

## 1) Título
Predição de Mortes por Tuberculose Utilizando Aprendizado de Máquina

## 2) Integrantes
Tales Hernandes – RA: 10408846 – E-mail: 10408846

## 3) Resumo
Este projeto tem como objetivo aplicar técnicas de Inteligência Artificial para analisar e prever o número estimado de mortes por tuberculose (todas as formas) a cada 100.000 habitantes em diferentes países e períodos históricos. Utilizando dados da Organização Mundial da Saúde (OMS) disponibilizados via Gapminder, serão explorados padrões temporais, regionais e socioeconômicos relacionados à tuberculose, com o intuito de identificar fatores críticos que afetam a mortalidade. Pretende-se aplicar modelos de Machine Learning para criar um sistema preditivo que auxilie no monitoramento e combate da doença.
## 4) Introdução

### a. Contextualização
A tuberculose é uma das doenças infecciosas mais letais do mundo, afetando milhões de pessoas todos os anos. Apesar dos avanços na medicina, ainda representa um grande desafio de saúde pública, especialmente em países de baixa e média renda.

### b. Justificativa
A análise de dados históricos pode auxiliar governos e organizações internacionais a direcionarem políticas públicas e recursos para o combate da tuberculose. O uso de Inteligência Artificial permite identificar padrões e prever cenários futuros, o que pode contribuir para a redução da mortalidade.

### c. Objetivo
Realizar uma análise exploratória dos dados históricos de mortalidade por tuberculose;
Aplicar modelos de Machine Learning (classificação/regressão) para prever a evolução da mortalidade;
Avaliar o desempenho dos modelos e interpretar os resultados obtidos.

### d. Opção do projeto
 Framework: utilização do scikit-learn para análise e modelagem preditiva.
 
## 5) Descrição do Problema
Apesar dos esforços da OMS e governos locais, a tuberculose continua a ser uma das principais causas de morte em diversos países. A previsão da mortalidade com base em dados históricos pode auxiliar na tomada de decisão e no direcionamento de recursos. O problema consiste em desenvolver um modelo de aprendizado de máquina capaz de prever a taxa de mortes por tuberculose em diferentes regiões.

## 6) Aspectos Éticos e Responsabilidade
O uso da IA em saúde exige responsabilidade. Modelos preditivos não substituem diagnósticos médicos, mas podem apoiar políticas públicas. É importante garantir que os dados sejam tratados de forma ética, evitando vieses geográficos ou socioeconômicos que possam comprometer a interpretação. Além disso, os resultados devem ser apresentados de forma transparente, sem criar pânico ou interpretações equivocadas.

## 7) Dataset, Análise Exploratória e Preparação dos Dados
O dataset utilizado foi obtido no portal Gapminder (https://www.gapminder.org/data/), com origem nos dados oficiais da Organização Mundial da Saúde (WHO) (https://www.who.int/tb/en/). Ele contém o número estimado de mortes por tuberculose (todas as formas) por 100.000 habitantes em diversos países e territórios, no período de 2000 a 2023.
O arquivo possui 214 linhas (países/regiões) e 24 colunas de anos (2000 a 2023), além da coluna de identificação do país.
Durante a análise exploratória:
Identificou-se que há valores ausentes em alguns anos iniciais (2000–2010), mas a partir de 2011 os dados estão completos.
Observou-se que a média global de mortalidade por tuberculose vem diminuindo desde 2000, embora alguns países, sobretudo na África Subsaariana, apresentem taxas ainda muito elevadas.
Em 2023, os países mais críticos incluem Lesoto, República Centro-Africana e Gabão, com valores superiores a 100 mortes por 100k habitantes.


Para a preparação dos dados:
Os valores ausentes foram tratados por meio de imputação pela média.
Foi feita a normalização (StandardScaler) para garantir escalas comparáveis entre as variáveis temporais.
Definiu-se como variáveis explicativas (X) os anos de 2000 a 2022, e como variável alvo (y) o ano de 2023, permitindo avaliar modelos de regressão para prever a mortalidade recente a partir de dados históricos.
Por fim, os dados foram divididos em treino (80%) e teste (20%), garantindo a avaliação adequada dos modelos de Machine Learning.
