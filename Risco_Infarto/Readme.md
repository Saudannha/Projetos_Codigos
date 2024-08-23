### Projeto da matéria de Ciência de Dados do 5º semestre do curso de Ciências da Computação da Unifaj - Unieduk
---
# Conjunto de Dados de Previsão de Risco de Ataque Cardíaco
Desbloqueando Insights Preditivos com Conjunto de Dados de Ataque Cardíaco Sintético Multifacetado.

## Sobre o conjunto de dados


### Contexto
O Conjunto de Dados de Previsão de Risco de Ataque Cardíaco serve como um recurso valioso para se aprofundar na intrincada dinâmica de saúde cardíaca e seus preditores. Ataques cardíacos, ou infarto do miocárdio, continuam a ser um problema de saúde global significativo, exigindo uma compreensão mais profunda de seus precursores e potenciais fatores mitigadores. Este conjunto de dados encapsula uma gama diversificada de atributos, incluindo idade, níveis de colesterol, pressão arterial, hábitos de fumar, padrões de exercícios, preferências alimentares e muito mais, como objetivo de elucidar a complexa interação dessas variáveis na determinação de probabilidade de um ataque cardíaco. Ao empregar análise preditiva e aprendizado de máquina neste conjunto de dados, pesquisadores e profissionais de saúde podem trabalhar em direção a estratégias proativas de prevensão e gerenciamento de doenças cardíacas. O conjunto de dados é uma prova de esforços coletivos para melhorar nossa compreensão da saúde cardiovascular e pavimentar o caminho para um futuro mais saudável.
### Conteúdo
Este conjunto de dados fornece uma gama abrangente de recursos relevantes para a saúde do coração e as escolhas de estilo de vida, abrangendo detalhes específicos do paciente, como idade, sexo, níveis de colesterol, pressão arterial, frequência cardiaca e indicadores como diabetes, histórico familiar, hábitos de fumar, obesidade e consumo de álcool. Além disso, fatores de estilo de vida como horas de exercício, hábitos alimentares, níveis de estresse e horas sedentárias estão incluídos. Aspectos médicos que incluem problemas cardíacos anteriores, uso de medicamentos e níveis de triglicerídeos são considerados. Aspectos socioeconômicos, como renda e atributos geaográficos, como país, continente e hemisfério, são incorporados. O conjunto de dados, que consiste em 8763 registros de pacientes de todo o mundo, culmina em um recurso crucial de classificação binária que denota a presença ou ausência de um risco de ataque cardíaco, fornecendo um recurso abrangente para análise preditiva e pesquisa em saúde cardiovascular.
### Glossário do Conjunto de Dados (em termos de coluna)
**Patient ID** - Identificador exclusivo para cada paciente
**Age** - Idade do paciente
**Sex** - Sexo do paciente (0: Masculino / 1: Feminino)
**Cholesterol** - Níveis de colesterol do paciente
**Heart Rate** - Frequência cardíaca do paciente
**Diabetes** - Se o paciente tem diabetes (Sim/Não)
**Family History** - História da família de problemas realcionados ao coração (1: Sim, 0: Não)
**Smoking** - Status de fumar do paciente (1:Fumante, 0: Não fumante)
**Obesity** - Estado de obesidade do paciente (1: Obesa, 0: Não obesa)
**Alcohol Consumption** - Nível de consumo de álcool pelo paciente (Nenhum/Leve/Moderado/Pesado)
**Exercice Hours Per Week** - Número de horas de exercícios por semana
**Diet** - Hábitos alimentares do paciente (0: Saudável / 1: Média / 2: Insalubre)
**Previous Heart Problems** - Problemas Cardíacos Anteriores do paciente (1: Sim, 0: Não)
**Medication Use** - Uso de Medicamentos pelo paciente (1: Sim, 0: Não)
**Stress Level** - Nível de Estresse relatado pelo paciente (1-10)
**Sedentary Hours Per Day** - Horas de atividades sedentárias por dia
**Income** - Nível de renda do paciente
**BMI** - Índice de Massa Corporal (IMC) do paciente
**Triglycerides** - Níveis de triglicerídeos do paciente
**Physical Activity Days Per Week** - Dias de atividades física por semana
**Sleep Hours Per Day** - Horas de sono por dia
**Heart Attack Risk** - Presença de risco de ataque cardíaco (1: Sim, 0: Não)

## Análise Detalhada do Código de Predição de Ataque Cardíaco

Este código utiliza Python e bibliotecas de aprendizado de máquina para analisar dados médicos e criar um modelo capaz de prever o risco de um paciente sofrer um ataque cardíaco. O código se divide em etapas principais:
**1. Coleta e Preparo dos Dados:**
- Os dados, provenientes de arquivos CSV chamados "train.csv", "test.csv" e "y_test.csv", são carregados utilizando a biblioteca Pandas.
- A coluna "PatientID", irrelevante para a predição, é removida.
- A qualidade dos dados é verificada, buscando por valores faltantes. Se encontrados, estes são preenchidos com a mediana dos valores da respectiva coluna.
- As variáveis categóricas, como sexo e histórico de tabagismo, são convertidas para representações numéricas através do One-Hot Encoding, preparando-as para o algoritmo de aprendizado de máquina.
**2. Investigando Relações nos Dados:**
- Gráficos como histogramas e scatter plots são gerados com o Matplotlib e Seaborn para visualizar a distribuição dos dados e identificar possíves relações entre as variáveis.
- A correlação entre as variáveis numéricas é analisada através de um mapa de calor (heatmap).
**3. Construindo e Treinando o Modelo Preditivo:**
- O código utiliza um algoritmo de Árvore de Decisão para construir o modelo preditivo.
- Os dados são divididos em conjuntos de treinamento e validação para avaliar a capacidade de generalização do modelo.
- O modelo é treinado com os dados de treinamento, aprendendo a classificar o risco de ataque cardíaco com base nos dados médicos e de estilo de vida.
**4. Avaliando a Performance do Modelo:**
- O modelo treinado é utilizado para fazer previsões nos dados de validação.
- A acurácia, que mede a porcentagem de previsões corretas, é calculada para determinar a performance do modelo.
**5. Prevendo o Risco de um Novo Paciente**
- Uma função interativa, prever_risco(), permite a entrada de dados de um novo paciente, como idade, colesterol, histórico familiar, etc.
- A função processa esses dados, aplicando as mesmas transformações realizadas nos dados de treinamento, e os utiliza no modelo para gerar a predição de risco de ataque cardíaco.
Em resumo, o código demonstra um processo completo de análise de dados e aprendizado de máquina para a predição de riscis à saúde, desde a manipulação e exploração dos dados até a construção e palicação de um modelo preditivo.
