# Desafio-DIO-PowerBI-Lucros-Vendas

Desafio: Criar um Relatório de Vendas e Lucros com Data Analytics no Power BI
Descrição do Desafio de Projeto
Objetivo:
Criar um relatório de vendas e lucros no Power BI, utilizando as melhores práticas de design e storytelling para apresentar os dados de forma clara e intuitiva para o cliente. O relatório deve incluir detalhes sobre os TOP3 produtos, principais países em termos de vendas e/ou lucro, um gráfico de dispersão sobre unidades vendidas e vendas por mês, além de visuais de agrupamentos e compartimentação de dados.

Diretrizes
Página de Detalhes:
Crie a página de detalhes conforme mostrado no desafio de projeto.
Disposição dos Visuais:
Pense na disposição dos visuais considerando como o cliente irá consumir o conteúdo.
O número de páginas pode variar dependendo da disposição dos visuais (até duas páginas).
Medidas Necessárias:
Crie as medidas necessárias para suportar os visuais.
Passo a Passo
1. Preparação do Ambiente
Abrir o Power BI:
Carregue os dados relevantes para o relatório, como a tabela Financial Sample.
2. Criação das Medidas Necessárias
Medidas DAX:
Crie as seguintes medidas para auxiliar na construção dos visuais:

-- Medida para o TOP3 Produtos por Vendas
Top3ProductsSales = 
CALCULATE(
    [Total Sales],
    TOPN(3, ALL(Financials[Product]), [Total Sales], DESC)
)

-- Medida para o TOP3 Produtos por Lucro
Top3ProductsProfit = 
CALCULATE(
    [Total Profit],
    TOPN(3, ALL(Financials[Product]), [Total Profit], DESC)
)

-- Medida para Vendas Totais
TotalSales = SUM(Financials[Sales])

-- Medida para Lucro Total
TotalProfit = SUM(Financials[Profit])

-- Medida para Unidades Vendidas Totais
TotalUnitsSold = SUM(Financials[Units Sold])

-- Medida para Vendas por Mês
SalesPerMonth = 
CALCULATE(
    [Total Sales],
    VALUES(Financials[Month])
)

-- Medida para Unidades Vendidas por Mês
UnitsSoldPerMonth = 
CALCULATE(
    [Total Units Sold],
    VALUES(Financials[Month])
)


3. Criação da Página de Detalhes
Título da Página: Detalhes de Vendas e Lucros

Adicione um título claro e descritivo para a página.
Visuais a Serem Incluídos:

TOP3 Produtos:

Gráfico de barras horizontal mostrando os TOP3 produtos por vendas.
Gráfico de barras horizontal mostrando os TOP3 produtos por lucro.
Principais Países em Termos de Vendas e/ou Lucro:

Mapa de calor ou gráfico de barras mostrando os principais países por vendas.
Mapa de calor ou gráfico de barras mostrando os principais países por lucro.
Gráfico de Dispersão:

Gráfico de dispersão mostrando unidades vendidas e vendas por mês.
Visuais de Agrupamentos de Dados:

Clustered column chart mostrando vendas agrupadas por segmentos.
Clustered column chart mostrando lucros agrupados por segmentos.
Visuais de Compartimentação dos Dados:

Treemap mostrando a distribuição das vendas por produto.
Treemap mostrando a distribuição do lucro por produto.
4. Estilização e Storytelling
Estilização Consistente:

Utilize cores, fontes e estilos consistentes para todos os visuais.
Posicione os elementos de forma lógica e esteticamente agradável.
Storytelling:

Crie uma história que conecte os diferentes visuais e ajude o usuário a entender os dados.
Utilize títulos, descrições e anotações para guiar o usuário através do relatório.
Exemplo de Storytelling
Título da Página: Detalhes de Vendas e Lucros

Introdução:
"Bem-vindo ao nosso relatório detalhado de vendas e lucros. Esta página fornece uma visão aprofundada dos produtos mais vendidos, principais países em termos de vendas e lucro, além de uma análise detalhada das vendas e unidades vendidas por mês."

Seção 1: TOP3 Produtos

Título: Produtos Mais Vendidos
Descrição: "Esta seção destaca os três produtos mais vendidos e os três produtos mais lucrativos, proporcionando uma visão clara sobre quais produtos estão impulsionando nosso desempenho."
Gráficos: Gráfico de barras horizontal para TOP3 produtos por vendas e lucro.
Anotação: "Note que o produto X é tanto o mais vendido quanto o mais lucrativo."
Seção 2: Principais Países em Termos de Vendas e/ou Lucro

Título: Principais Países
Descrição: "Esta seção mostra os principais países em termos de vendas e lucro, permitindo identificar mercados chave e oportunidades de crescimento."
Gráficos: Mapa de calor ou gráfico de barras para vendas e lucro por país.
Anotação: "Os países Y e Z são nossos maiores mercados, com vendas e lucros significativos."
Seção 3: Gráfico de Dispersão

Título: Vendas e Unidades Vendidas por Mês
Descrição: "O gráfico de dispersão abaixo mostra a relação entre unidades vendidas e vendas por mês, ajudando a identificar padrões sazonais e tendências de vendas."
Gráficos: Gráfico de dispersão para unidades vendidas e vendas por mês.
Anotação: "Observe o aumento nas vendas durante os meses de pico de compras."
Seção 4: Agrupamentos de Dados

Título: Análise de Segmentos
Descrição: "Esta seção agrupa os dados de vendas e lucros por segmento, proporcionando insights sobre o desempenho de diferentes áreas de negócios."
Gráficos: Clustered column chart para vendas e lucros por segmento.
Anotação: "O segmento A mostra um desempenho consistente, enquanto o segmento B apresenta oportunidades de melhoria."
Seção 5: Compartimentação dos Dados

Título: Distribuição das Vendas e Lucros
Descrição: "Os treemaps abaixo mostram a distribuição das vendas e lucros por produto, permitindo uma análise visual rápida e intuitiva."
Gráficos: Treemaps para distribuição das vendas e lucros por produto.
Anotação: "Os produtos X e Y são os principais contribuintes para nossas vendas e lucros."
Exemplo de README

# Projeto: Relatório de Vendas e Lucros com Data Analytics

## Descrição

Este projeto consiste na criação de um relatório detalhado de vendas e lucros no Power BI, utilizando as melhores práticas de design e storytelling para apresentar os dados de forma clara e intuitiva.

## Páginas do Relatório

### Página 1: Detalhes de Vendas e Lucros

**Visuais Incluídos:**
- **TOP3 Produtos por Vendas e Lucro:**
  - Gráfico de barras horizontal mostrando os três produtos mais vendidos.
  - Gráfico de barras horizontal mostrando os três produtos mais lucrativos.

- **Principais Países em Termos de Vendas e Lucro:**
  - Mapa de calor ou gráfico de barras mostrando os principais países por vendas.
  - Mapa de calor ou gráfico de barras mostrando os principais países por lucro.

- **Gráfico de Dispersão:**
  - Gráfico de dispersão mostrando unidades vendidas e vendas por mês.

- **Agrupamentos de Dados:**
  - Clustered column chart mostrando vendas e lucros por segmento.

- **Compartimentação dos Dados:**
  - Treemap mostrando a distribuição das vendas por produto.
  - Treemap mostrando a distribuição do lucro por produto.

## Funcionalidades e Fórmulas DAX Utilizadas

- **Medidas DAX:**
  - Criação de medidas para TOP3 produtos, vendas totais, lucro total, unidades vendidas totais, vendas por mês e unidades vendidas por mês.

## Storytelling (Continuação)

**Seção 3: Gráfico de Dispersão**
- **Título:** Vendas e Unidades Vendidas por Mês
- **Descrição:** "O gráfico de dispersão abaixo mostra a relação entre unidades vendidas e vendas por mês, ajudando a identificar padrões sazonais e tendências de vendas."
- **Gráficos:** Gráfico de dispersão para unidades vendidas e vendas por mês.
- **Anotação:** "Observe o aumento nas vendas durante os meses de pico de compras."

**Seção 4: Agrupamentos de Dados**
- **Título:** Análise de Segmentos
- **Descrição:** "Esta seção agrupa os dados de vendas e lucros por segmento, proporcionando insights sobre o desempenho de diferentes áreas de negócios."
- **Gráficos:** Clustered column chart para vendas e lucros por segmento.
- **Anotação:** "O segmento A mostra um desempenho consistente, enquanto o segmento B apresenta oportunidades de melhoria."

**Seção 5: Compartimentação dos Dados**
- **Título:** Distribuição das Vendas e Lucros
- **Descrição:** "Os treemaps abaixo mostram a distribuição das vendas e lucros por produto, permitindo uma análise visual rápida e intuitiva."
- **Gráficos:** Treemaps para distribuição das vendas e lucros por produto.
- **Anotação:** "Os produtos X e Y são os principais contribuintes para nossas vendas e lucros."

## Conclusão

Este projeto focou na criação de um relatório de vendas e lucros utilizando o Power BI, seguindo as melhores práticas de design e storytelling. O relatório visa fornecer insights valiosos para tomada de decisões estratégicas, destacando os produtos mais vendidos, os principais mercados em termos de vendas e lucro, além de análises detalhadas de vendas por mês, segmentos de negócios e distribuição de vendas por produto.

---

Este modelo segue as diretrizes estabelecidas para o desafio de criar um relatório de Vendas e Lucros com Data Analytics no Power BI.
