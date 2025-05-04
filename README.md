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

Este relatório tem como objetivo expor o resultado das análises realizadas utilizando como base os dados de cada uma das lojas, fornecidos através da planilhas fornecidas pelo cliente.
O objeto da análise é identificar qual loja possui o menor desempenho em termos de faturamento, volume de vendas, categorias de produtos mais e menos vendidos e frete médio cobrado.

Baseados nestas informações preliminares, foram criadas as dimensões necessárias que serviram de base para a geração dos relatórios apresentados em cada ponto analisado abaixo.

#### Faturamento

Considerando o item faturamento total, fiz uma comparação entre as 4 lojas da rede, e as análises evidenciam que a loja 4 apresentou um faturamento total menor comparado às demais lojas:

Loja 1  -> ![chrome_XsggOEnOAg](https://github.com/user-attachments/assets/007e3295-21b0-4fc3-a705-81a40b64fc91)

Loja 2  -> ![chrome_SlQZaXiYdL](https://github.com/user-attachments/assets/34e398f6-8690-41aa-a8f1-7813729abb9f)

Loja 3  -> ![chrome_yX9s8AiOLB](https://github.com/user-attachments/assets/5789875e-679c-4fa1-84ab-10a9aef94aa4)

Loja 4  -> ![chrome_KY9UNc4Gy8](https://github.com/user-attachments/assets/d7ca8f21-0830-49be-a96f-8c3b01e58b7b)    

#### Volume de Vendas

Por consequencia, a loja 4 apresenta o menor volume de vendas e o menor preço médio, o que pode indicar um menor potencial de crescimento ou lucratividade em comparação com as outras lojas nos próximos anos. 

![chrome_6BgG7xKc3i](https://github.com/user-attachments/assets/3e9709d7-cda2-4e06-826e-1c8dbbb0626c)

#### Preço Médio

Abaixo, segue o valor do preço médio por loja, e novamente a loja 4 apresenta o menor ticket médio de vendas:

![chrome_WIVLZ82kjX](https://github.com/user-attachments/assets/d15b31e5-d7ba-4652-90cd-b77e812d03ef)

#### Faturamento por categoria

Analisando visualmente, o gráfico abaixo mostra o total de vendas (R$) por categorias em cada loja, percebemos que a loja 4 não performa bem nas categorias que mais vende nas demais lojas, a saber, eletrônicos e eletrodomésticos:

![chrome_8lqkMY4SHZ](https://github.com/user-attachments/assets/af2d097c-7a6d-4457-9c37-793f31a55fad)

#### Quantidade vendida por categoria

O gráfico abaixo mostra o percentual quantitativo da amostra, não considerando o valor faturado por categoria, o qual é exibido no gráfico acima:

![chrome_o7I8GKFkUU](https://github.com/user-attachments/assets/203c6191-310a-496d-bb1e-98cfaf09e607)

#### Avaliações dos clientes

A análise de avaliações dos clientes também indicou que a loja 4 está com a segunda posição de pior avaliada, em comparação com as demais lojas.

![chrome_RMLSZqutkf](https://github.com/user-attachments/assets/692e0284-4169-4f99-ab76-e6068316c207)

As avalições podem fornecer alguns insights interessantes que valeria uma análise mais aprofundada. Tais insights são:

1 - A loja possui produtos de última geração na categoria de eletrônicos?    
2 - A loja possui produtos com preços competitivos nas categorias eletrônicos e eletrodomésticos?    
3 - A loja possui um atendimento cativante e vendedores atenciosos?    
4 - A estrutura da loja é segura, confortável e receptiva?    
5 - A loja possui diversidade de meios de pagamento que facilitem a compra?    
6 - A loja faz promoções e divulgação dos seus produtos de forma adequada?    
7 - A loja cumpre com os prazos de entrega acordados com seus clientes?    
8 - A loja entrega os produtos vendidos corretamente e em boas condições?    
9 - A loja oferece algum serviço de pós venda aos seus clientes?    
10 - A loja sabe fidelizar o cliente?    

Outro ponto de reflexão sobre o resultado das análises. Sabemos que o dono da loja precisa decidir qual loja vender para adquirir o valor para um novo empreendimento. A pergunta que fica é: A venda pedido na venda da loja com menor faturamento será o valor necessário para o novo empreendimento, pois talvez ele não consiga vender tal loja por um valor adequado.
Algumas hipóteses levantadas para tal indagação são:

1 - A loja está bem localizada?    
2 - A loja possui clientes com renda superior a 1 salário mínimo?    
3 - A loja possui concorrentes do mesmo porte na mesma região que ela se encontra?    
4 - A loja possui a formação adequada para o preço de seus produtos?

#### Frete médio por loja

O frete médio não foi considerado um fator relevante na análise, pois a informação gerada com base no percentual médio cobrado pelo faturamento por loja, não fornece muitos indícios se são ou não aplicáveis na decisão de venda, uma vez que poderíamos considerar outros dados como localização das lojas, volumes dos produtos, quantidades por região, distância, entre outros.

O gráfico abaixo exibe o percentual médio do frete pelo faturamento total no período completo.

![chrome_F5umeieazl](https://github.com/user-attachments/assets/71b4539c-1624-4c80-aa75-1069f7b7921e)

#### Conclusão da análise

Com base no resultados das dimensões criadas a partir das análises feitas e dos gráficos apresentados acima, bem como a explicação de cada um, conclui que a loja que parece ser a melhor candidata para venda é a Loja 4. 

### Pessoa desenvolvedora realizadora do projeto

Este projeto foi desenvolvido como parte do programa de treinamento da Oracle One em parceria com a Alura Latam que participo como estudante de Data Science. A ClearSale possui parceira com as empresas Oracle e Alura, e por isso disponibiliza aos seus colaboradores, através do programa ClearOne toda a trilha de treinamento em Data Science pela plataforma da Alura.

Prazer, me chamo Rosane Marchand!

Para me conhecer melhor, segue o meu perfil no Linkedin com detalhes da minha trajetória profissional - https://www.linkedin.com/in/rosane-marchand-analista-qualidade-sr/

### Créditos

Os ícones utilizados neste documento foram obtidos do site: <a href="https://br.freepik.com/vetores-gratis/apresentacao-azul-e-cinza-cor-icons-set_959361.htm">Imagem de ibrandify no Freepik</a>
