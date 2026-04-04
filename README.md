# Projeto de Estatística

Análise exploratória de dados sobre diabetes nos Estados Unidos com base no dataset `BRFSS 2015`.

## Visão geral

Este projeto investiga como indicadores de saúde, hábitos de vida e fatores socioeconômicos aparecem relacionados ao diabetes. A proposta central foi usar análise exploratória de dados para comparar grupos, identificar padrões e interpretar os resultados a partir de medidas estatísticas e visualizações.

## Objetivo

O objetivo do trabalho é entender quais fatores aparecem mais associados ao diabetes ao longo da base analisada.

Para isso, o notebook foi organizado para responder quatro perguntas centrais:

1. Quais fatores de risco estão mais relacionados ao diabetes?
2. Qual a relação entre IMC, atividade física e diabetes?
3. Qual a relação entre renda, educação e diabetes?
4. Qual a relação entre sexo, renda e diabetes?

## Hipóteses do grupo

Antes da análise, o grupo trabalhou com as seguintes hipóteses:

1. Pressão alta e colesterol alto estariam entre os fatores mais associados ao diabetes.
2. Grupos com maior IMC e menor prática de atividade física apresentariam maior proporção de diabetes.
3. Níveis mais baixos de renda e escolaridade estariam associados a percentuais maiores de diabetes.
4. A relação entre renda e diabetes poderia variar entre homens e mulheres, com maior concentração nas faixas de renda mais baixas.

## Estrutura do projeto

Na raiz do projeto ficam os arquivos principais da entrega:

- `PROJETO_ESTATISTICA.ipynb`: notebook principal da análise
- `diabetes_012_health_indicators_BRFSS2015.csv`: base de dados usada no notebook
- `README.md`: visão geral do projeto
- `.gitignore`: regras para ignorar arquivos temporários e auxiliares

## Base de dados

O projeto utiliza o dataset `Diabetes Health Indicators Dataset`, derivado do `BRFSS 2015`. Cada linha da base representa uma pessoa.

| Indicador | Valor |
|---|---:|
| Registros originais | 253.680 |
| Duplicatas removidas | 23.899 |
| Registros após limpeza | 229.781 |
| Sem diabetes | 82,71% |
| Pré-diabetes | 2,01% |
| Diabetes | 15,27% |

## O que foi feito no notebook

O notebook segue uma sequência lógica de preparação e análise:

- carregamento da base de dados
- verificação de valores nulos
- identificação e remoção de duplicatas
- conversão das colunas para formato numérico
- criação da variável auxiliar `diabetes`
- cálculo de medidas de centralização, posição e dispersão
- análise de correlação
- normalização Min-Max do IMC
- construção de gráficos para apoiar cada hipótese

## Principais resultados

| Hipótese | Resultado principal | Leitura final |
|---|---|---|
| Fatores de risco | Pressão alta: 6,93% → 25,29% | Confirmada |
| Fatores de risco | Colesterol alto: 9,04% → 23,15% | Confirmada |
| IMC e atividade física | IMC médio cresce de 28,03 para 31,96 | Confirmada |
| Renda e educação | Menor renda: 24,34% / Maior renda: 9,81% no total | Confirmada |
| Sexo e renda | Na menor renda, feminino 25,84% e masculino 21,18% | Não confirmada na forma proposta |

## Síntese das análises

- Pressão alta e colesterol alto apareceram com associação mais forte ao diabetes.
- O IMC médio aumenta conforme o grupo avança de sem diabetes para diabetes.
- A prática de atividade física é menor nos grupos com diabetes.
- Faixas mais baixas de renda e escolaridade apresentaram percentuais maiores de diabetes.
- A hipótese sobre homens de baixa renda não se confirmou da forma inicialmente proposta.

## Como executar

Abra o arquivo `PROJETO_ESTATISTICA.ipynb` no Jupyter Notebook, JupyterLab ou Google Colab e execute as células em ordem. O notebook foi configurado para ler automaticamente o arquivo `diabetes_012_health_indicators_BRFSS2015.csv` a partir da raiz do projeto.

## Observação final

Este é um projeto de análise exploratória de dados. Por isso, os resultados devem ser lidos como relações observadas na base, e não como prova definitiva de causalidade.
