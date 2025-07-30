Este projeto realiza uma análise preditiva da renda utilizando regressão linear múltipla com variáveis socioeconômicas. O objetivo é identificar os fatores que mais influenciam a renda de uma pessoa, ajustando diferentes versões do modelo.

Base de Dados
Nome: previsao_de_renda.csv
Dados fictícios sobre:
características pessoais (idade, sexo, filhos, etc.)
condições de vida (tipo de residência, posse de imóvel/veículo)
renda mensal

Etapas do Projeto
1. Pré-processamento
Preenchimento de valores ausentes com média (tempo_emprego)

Conversão de variáveis categóricas para o tipo category

Análise de frequência das variáveis

2. Criação de Modelos
modelo_0: Regressão com todas as variáveis (sem tratamento especial)

modelo_1: Inclui a variável tipo_residência com categoria "Casa" como grupo de referência (baseline)

modelo_2: Modelo sem a variável tipo_residência

modelo_3: Modelo reduzido com as variáveis mais significativas

3. Transformações
A variável dependente renda é transformada com np.log(renda) para garantir normalidade dos resíduos.

Ferramentas e Bibliotecas
pandas, numpy – Manipulação de dados

statsmodels – Modelagem estatística

patsy – Construção de matrizes de design para fórmulas estatísticas

matplotlib, seaborn – Visualizações

Métricas e Avaliação
Coeficientes estimados

p-valores e significância estatística

R² e R² ajustado

Comparação entre modelos via exclusão de variáveis

Conclusões
O modelo identificou variáveis significativas na previsão da renda, como:

tipo de renda

estado civil

posse de veículo

idade e tempo de emprego

A transformação log(renda) melhora a adequação do modelo.

Testes com diferentes baseline em variáveis categóricas demonstram impacto na interpretação dos coeficientes.
