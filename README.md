# Data Science - Primeira análise de dados com Python, Pandas e Matplotlib

![lampada](https://github.com/user-attachments/assets/d8d1d1ed-fcda-4d17-b836-05f71bd6712c)
## Qual o objetivo deste projeto de Análise de Dados? 

Este projeto tem como objetivo ajudar o dono de uma rede de lojas chamada Alura Store a identificar qual loja ele deve vender, afim de obter recursos para investir em um novo empreendimento.

## Quais os componentes utilizados para a realização da Análise de Dados?

O desafio consiste em analisar os dados de vendas, desempenho e avaliações das 4 lojas fictícias da Alura Store.
Para isso, foram disponibilizadas 4 planilhas contendo os dados de Produtos, Categorias, Preço, Localização dos Clientes, Formas de Pagamento e Avaliação das Compras, entre outros, em um período de 3 anos, compreendidos entre 2020 e 2022.

## Primeiros passos para organizar e iniciar o trabalho de análise dos dados

Eu, como cientista de dados responsável do projeto tenho a missão de identificar a loja com menor eficiência e apresentar uma recomendação final baseada na análise dos  dados fornecidos.
Para isso, foi realizado um estudo prévio das bases fornecidas, a fim de identificar padrões de comportamento e desvios.
Após o estudo, foi a carga dos dados para o Colab, ferramenta utilizada para a realização das amostras de dados e geração dos gráficos.
Foram realizadas as importações e inicialização das bibliotecas necessárias, como o Pandas e a Matplotlib.
Na sequencia, foram realizadas algumas amostras utilizando os dados fornecidos, através da geração de listas, listas de listas, lista de tuplas e dicionários para agrupar os valores dos somatórios e médias dos dados que foram usados para a montagems dos gráficos.

### Primeiras análises

Através das primeiras dimensões o criadas, foi possível levantar os dados de faturamento de cada uma das 4 lojas, por ano, a saber, 2020, 2021 e 2022, e ao final foram gerados os dados do faturamento total do período completo por loja. 
Esta análise mostrou que no ano de 2021 houve um aumento no faturamento em comparação com o ano anterior e uma queda no ano de 2022 em comparação com o ano de 2021, conforme o gráfico abaixo:

![chrome_pY5yEXarzF](https://github.com/user-attachments/assets/1209784f-73de-4a8c-bfaa-d09047ae2b24)

### Médias obtidas dos pedidos e preço médio por loja

Foram levantadas as médias dos pedidos por loja, bem como o preço médio das vendas por loja. Esta visão indica que a loja com maior faturamento através da quantidade de pedidos com valor médio por vendas maior, em comparação com as demais, é mais lucratividade e possui uma base de clientes consolidada. O resultado foi apresentado no gráfico abaixo:

![chrome_tUitEeqgT5](https://github.com/user-attachments/assets/06a55a98-5de7-42e4-ae76-9f5de32bcc3e)

### Análise do período mensal de faturamento

O objetivo desta análise é ter uma visão geral da sazonalidade de vendas das 4 lojas no período total analisado. Escolhi o gráfico de linhas para visualizar os períodos de maior e menor venda por loja.
O resultado pode ser visto no gráfico abaixo:

![chrome_NLvuX21OyM](https://github.com/user-attachments/assets/1375b6a6-6177-437c-ad9c-91206920c85a)

### Análise das vendas por categoria

Analisar as categorias com maior e menor venda em cada uma das lojas nos fornece uma visão da preferência dos consumidores, além de identificar quais os itens que garantem um valor médio de vendas.
Neste primeiro gráfico, podemos identificar que a categoria com maior volume de vendas é a de Eletrônicos.

![chrome_4WwGKTvJNo](https://github.com/user-attachments/assets/34d6d5ca-b787-42d9-8ed5-53acbe830ff9)

Já no segundo gráfico apresentado abaixo, a categoria que se destaca em volume financeiro é de Eletrodomésticos, seguida pela categoria de Eletrônicos.

![chrome_aCFPnB3rCX](https://github.com/user-attachments/assets/a73e19b4-5082-45e1-857d-25a632ae6eed)


### Análise das avaliações por loja

A planilha recebida continha uma coluna de avaliações recebidas dos clientes, onde constavam números de 1 a 5, sem identificação. Contatamos o cliente para identificar qual a legenda adequada para cada número da coluna, e ficou esclarecido que as seguintes legendas:

1 - Muito ruim    
2 - Ruim    
3 - Neutra    
4 - Boa    
5 - Muito boa    

Desta forma, foi possível realizar a análise comparando a quantidade de avaliações recebidas nas duas principais categorias, a saber: Muito ruim e Muito boa, conforme o gráfico abaixo:

![chrome_E1ZwoeGjfe](https://github.com/user-attachments/assets/bcb45e7e-e307-4f42-812c-def61fc2e656)

Com este gráfico, identificamos que a loja com maior número de avaliações negativas é a loja 1, seguida pela loja 4. Também identificamos que a maior quantidade de avaliações positivas está na loja 3, seguida pela loja 2, conforme resultado da execução da análise:

![chrome_k4OTqH4X7h](https://github.com/user-attachments/assets/2466b920-0c44-4e29-9f43-9ec21f8a5577)

### Análise do frete cobrado por loja

A análise do frete considerou apenas a proporcionalidade entre o faturamento total por loja e o percentual do frete cobrado pelas lojas. 
A análise não considerou qualquer informação relativa a tipos de produtos entregues e distâncias, devido à falta de informações adicionais nas bases.

O resultado da análise pode ser visualizado no gráfico abaixo:

![chrome_SAVBKYLLXm](https://github.com/user-attachments/assets/9801f9cd-4d54-4336-8d68-f0b97d508430)

# Conclusões

![relatorio](https://github.com/user-attachments/assets/615e83b3-5d92-466f-aa26-5da5a3c1a86f)
## Relatório final baseado no resultado das análises:

Com base na análise, a loja que parece ser a melhor candidata para venda é a Loja 4. Ela apresenta o menor total de vendas e o menor preço médio, o que pode indicar um menor potencial de crescimento ou lucratividade em comparação com as outras lojas.

Como apresentar ao cliente:

Resumo Inicial: Apresente a tabela analise_lojas_df para dar uma visão geral do desempenho das lojas.
Gráfico de Vendas por Categoria: Explique quais categorias são mais fortes em cada loja e se há alguma que está performando mal na Loja 4.
Gráfico de Evolução das Vendas: Mostre a tendência de vendas ao longo do tempo, destacando se a Loja 4 está em declínio ou estagnada.
Gráfico de Avaliação Média: Compare a satisfação dos clientes entre as lojas. Se a Loja 4 tiver uma avaliação mais baixa, isso pode reforçar a decisão de vendê-la.
Análise de Pagamento: Apresente os dados sobre os tipos de pagamento, mostrando se a Loja 4 está perdendo vendas por não oferecer opções de pagamento adequadas.
Conclusão: Recomende a venda da Loja 4, justificando a decisão com os dados e gráficos apresentados.

