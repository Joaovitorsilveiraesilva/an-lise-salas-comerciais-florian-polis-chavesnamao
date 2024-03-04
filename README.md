# Tableau e Web scraping: Análise das salas comerciais à venda em Florianópolis
## Apresentação
Este trabalho tem como objetivo a retirada e análise de 1485 instâncias de vendas de salas comerciais do site chavesnamao de imóveis (https://www.chavesnamao.com.br/sala-comercial-a-venda/sc-florianopolis/). 
Na primeira parte retirei com a técnica de web scraping os dados dos imóveis referentes a (caracteristicas [metro quadrado, número de salas, número de banheiros e número de garagens], descrição, bairro, preço, preço do condominio e endereço).
Na segunda parte, transformei algumas variáveis para melhor manuseio e também através da biblioteca geopy consegui pegar a latitude e longitude dos endereços.
Na terceira parte fiz uma análise suscita dos preços dos imóveis em relação a localização
Na última parte fiz um dashboard com Tableu do mapa dos imóveis em florianópolis pela sua localização. Nesse dashboard é possível aplicar filtros por bairro e range de preços

## Web Scraping
Nessa primeira parte usei a biblioteca beautifulsoup para retirada das informações das instâncias de imóveis do site e também salvei em um dataframe

Para cada instancia do Dataframe:

Azul: Refere-se as caracteristicas

Verde: Refere-se a descrição

Roxo: Refere-se ao bairro

Amarelo: Refere-se ao preço

Marrom: Refere-se ao preço condominio

Vermelho: Refere-s ao endereço

![Informações retiradas](https://raw.githubusercontent.com/Joaovitorsilveiraesilva/an-lise-salas-comerciais-florian-polis-chavesnamao/main/oquefoiretirado.png)

Observações:

Nem todas caracteristicas são semelhantes, algumas possuem só o m² com o número de banheiros. As instâncias completas possuem o m², o número de banheiro e o número de salas.

Quando não especificado o preço do condominio, optei por marcar o preço como zero.

A descrição também não é uniforme, ela varia de acordo com a pessoa que anuncia.

Tomei cuidado para filtrar somente os imóveis a venda, excluindo os de aluguel.

link : https://github.com/Joaovitorsilveiraesilva/an-lise-salas-comerciais-florian-polis-chavesnamao/blob/main/p1-web_scrap-salas-comerciais-florian%C3%B3polis-chavesnamao.ipynb

## Data Feature

Nessa segunda parte transformei as variáveis para facilitação e manipulação dos dados. Também através da biblioteca geopy, consegui retirar a localização dos endereços e dos bairros.

link: https://github.com/Joaovitorsilveiraesilva/an-lise-salas-comerciais-florian-polis-chavesnamao/blob/main/p2-data_feature-salas-comerciais-florian%C3%B3polis-chavesnamao.ipynb

## Análise exploratória

Na terceira parte fiz uma breve análise exploratória para ver o preço por m² médio por bairro. Também fiz uma regressão do m² dos imóveis contra o preço

link: https://github.com/Joaovitorsilveiraesilva/an-lise-salas-comerciais-florian-polis-chavesnamao/blob/main/p3-Analise-explorat%C3%B3ria-salas-comerciais-florian%C3%B3polis-chavesnamao.ipynb

## Mapa com Tableu

Na última parte fiz um dashboard interativo em Tableu, onde é possível aplicar filtros a respeito do bairro e do preço do imóvel. Esse dashboard contém as informações do preço do imóvel, m², bairro, localização por latitude e longitude.

![Dashboard Tableu](https://raw.githubusercontent.com/Joaovitorsilveiraesilva/an-lise-salas-comerciais-florian-polis-chavesnamao/main/mapa%20tableau.png)

Você pode interagir com o dashboard através desse link:

https://public.tableau.com/app/profile/jo.o.vitor.silveira.e.silva/viz/PreosalascomerciaisvendaFlorianpolis/dashboard

