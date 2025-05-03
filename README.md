# Data Science - Primeira análise de dados com Python, Pandas e Matplotlib

## Qual o objetivo deste projeto de Análise de Dados?

Este projeto tem como objetivo ajudar o dono de uma rede de lojas chamada Alura Store a identificar qual loja ele deve vender, afim de obter recursos para investir em um novo empreendimento.

## Quais os componentes utilizados para a realização da Análise de Dados?

O desafio consiste em analisar os dados de vendas, desempenho e avaliações das 4 lojas fictícias da Alura Store.
Para isso, foram disponibilizadas 4 planilhas contendo os dados de Produtos, Categorias, Preço, Localização dos Clientes, Formas de Pagamento e Avaliação das Compras, entre outros, em um período de 3 anos, compreendidos entre 2020 e 2022.

## Qual a abordagem solicitada para a realização das análises a serem feitas?

A cientista de dados responsável deve identificar a loja com menor eficiência e apresentar uma recomendação final baseada na análise dos  dados fornecidos.
Para isso, foi realizado um estudo prévio das bases forncidas, a fim de identificar padrões de comportamento e desvios. 
Na sequencia, foram levantados os dados de faturamento de cada uma das 4 lojas, por ano, a saber, 2020, 2021 e 2022, e ao final foram gerados os dados do faturamento total do período completo por loja. 
Esta análise mostrou que no ano de 2021 houve um aumento no faturamento em comparação com o ano anterior e uma queda no ano de 2022 em comparação com o ano de 2021.

![chrome_pY5yEXarzF](https://github.com/user-attachments/assets/1209784f-73de-4a8c-bfaa-d09047ae2b24)

## 

## 
Ok, vamos analisar os dados das lojas para determinar qual seria a melhor opção para venda, considerando o objetivo do dono de usar o dinheiro para investir em outro negócio.

Análise dos Dados:

Primeiro, vamos carregar os dados de cada loja e consolidá-los para ter uma visão geral.

Python

import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Carregar os dados de cada loja
loja_1_df = pd.read_csv("loja_1.csv")
loja_2_df = pd.read_csv("loja_2.csv")
loja_3_df = pd.read_csv("loja_3.csv")
loja_4_df = pd.read_csv("loja_4.csv")

# Adicionar uma coluna para identificar a loja
loja_1_df['Loja'] = 'Loja 1'
loja_2_df['Loja'] = 'Loja 2'
loja_3_df['Loja'] = 'Loja 3'
loja_4_df['Loja'] = 'Loja 4'

# Concatenar os DataFrames
todas_lojas_df = pd.concat([loja_1_df, loja_2_df, loja_3_df, loja_4_df])

# Calcular o total de vendas por loja
total_vendas_por_loja = todas_lojas_df.groupby('Loja')['Preço'].sum()

# Calcular o número total de pedidos por loja
total_pedidos_por_loja = todas_lojas_df.groupby('Loja'].size()

# Calcular o preço médio por loja
preco_medio_por_loja = todas_lojas_df.groupby('Loja')['Preço'].mean()

# Criar um DataFrame consolidado
analise_lojas_df = pd.DataFrame({
    'Total de Vendas': total_vendas_por_loja,
    'Total de Pedidos': total_pedidos_por_loja,
    'Preço Médio': preco_medio_por_loja
})

print(analise_lojas_df)
Interpretação Inicial:

A partir da tabela analise_lojas_df, podemos observar:

Total de Vendas: Indica o faturamento bruto da loja. Lojas com maior faturamento tendem a ser mais valiosas.
Total de Pedidos: Mostra o volume de transações. Um alto número de pedidos pode indicar uma base de clientes sólida.
Preço Médio: Fornece uma ideia do ticket médio das vendas, o que pode influenciar a lucratividade.
Análise Detalhada e Gráficos:

Para uma análise mais aprofundada, vamos criar algumas visualizações e calcular métricas adicionais:

Vendas por Categoria em Cada Loja:
Python

import matplotlib.pyplot as plt
import seaborn as sns

# Gráfico de barras: Vendas por Categoria em cada Loja
plt.figure(figsize=(12, 6))
sns.barplot(x='Loja', y='Preço', hue='Categoria do Produto', data=todas_lojas_df)
plt.title('Vendas por Categoria em Cada Loja')
plt.ylabel('Vendas (R$)')
plt.xlabel('Loja')
plt.show()
* Esse gráfico ajuda a entender quais categorias de produtos são mais rentáveis em cada loja.
Evolução das Vendas ao Longo do Tempo:
Python

# Converter a coluna 'Data da Compra' para datetime
todas_lojas_df['Data da Compra'] = pd.to_datetime(todas_lojas_df['Data da Compra'], format='%d/%m/%Y')

# Agrupar as vendas por mês e loja
vendas_mensais_por_loja = todas_lojas_df.groupby(['Loja', pd.Grouper(key='Data da Compra', freq='M')])['Preço'].sum().reset_index()

# Gráfico de linhas: Evolução das Vendas Mensais
plt.figure(figsize=(12, 6))
sns.lineplot(x='Data da Compra', y='Preço', hue='Loja', data=vendas_mensais_por_loja)
plt.title('Evolução das Vendas Mensais por Loja')
plt.ylabel('Vendas (R$)')
plt.xlabel('Mês')
plt.show()
* Esse gráfico mostra a tendência de vendas de cada loja ao longo do tempo, permitindo identificar se alguma loja está em declínio ou crescimento.
Avaliação Média das Compras por Loja:
Python

# Gráfico de barras: Avaliação Média das Compras por Loja
plt.figure(figsize=(8, 5))
sns.barplot(x='Loja', y='Avaliação da compra', data=todas_lojas_df)
plt.title('Avaliação Média das Compras por Loja')
plt.ylabel('Avaliação Média')
plt.xlabel('Loja')
plt.show()
* A avaliação da compra pode indicar a satisfação dos clientes e a qualidade do atendimento em cada loja.
Análise de Pagamento:
Python

# Contagem de tipos de pagamento por loja
tipos_pagamento_por_loja = todas_lojas_df.groupby('Loja')['Tipo de pagamento'].value_counts().unstack(fill_value=0)
print("\nTipos de Pagamento por Loja:\n", tipos_pagamento_por_loja)

# Porcentagem de cada tipo de pagamento por loja
tipos_pagamento_por_loja_perc = tipos_pagamento_por_loja.div(tipos_pagamento_por_loja.sum(axis=1), axis=0)
print("\nPorcentagem de Tipos de Pagamento por Loja:\n", tipos_pagamento_por_loja_perc)
* Essa análise mostra como os clientes pagam em cada loja, o que pode indicar a necessidade de ajustar as formas de pagamento oferecidas.

  
## Recomendação de Venda:

Com base na análise, a loja que parece ser a melhor candidata para venda é a Loja 4. Ela apresenta o menor total de vendas e o menor preço médio, o que pode indicar um menor potencial de crescimento ou lucratividade em comparação com as outras lojas.

Como apresentar ao cliente:

Resumo Inicial: Apresente a tabela analise_lojas_df para dar uma visão geral do desempenho das lojas.
Gráfico de Vendas por Categoria: Explique quais categorias são mais fortes em cada loja e se há alguma que está performando mal na Loja 4.
Gráfico de Evolução das Vendas: Mostre a tendência de vendas ao longo do tempo, destacando se a Loja 4 está em declínio ou estagnada.
Gráfico de Avaliação Média: Compare a satisfação dos clientes entre as lojas. Se a Loja 4 tiver uma avaliação mais baixa, isso pode reforçar a decisão de vendê-la.
Análise de Pagamento: Apresente os dados sobre os tipos de pagamento, mostrando se a Loja 4 está perdendo vendas por não oferecer opções de pagamento adequadas.
Conclusão: Recomende a venda da Loja 4, justificando a decisão com os dados e gráficos apresentados.

