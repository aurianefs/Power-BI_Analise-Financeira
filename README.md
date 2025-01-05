# Dashboard de Análise Financeira

Este dashboard foi criado para fornecer uma visão abrangente da saúde financeira da empresa, analisando receitas, despesas, margem de lucro, distribuição de despesas e receitas por componente, identificando os principais segmentos e permitindo a análise por diferentes períodos.

## Fontes de Dados

*   Banco de dados ou arquivo (CSV) contendo informações financeiras, incluindo:
    *   Data da transação
    *   Valor da receita
    *   Valor da despesa
    *   Componente da receita 
    *   Componente da despesa 
    *   Segmento

## Visualizações

*   **Total de Receitas:**
    *   Cartão (KPI) mostrando o valor total das receitas no período analisado.
    *   Gráfico de barras mostrando a evolução das receitas ao longo do tempo.
*   **Total de Despesas:**
    *   Cartão (KPI) mostrando o valor total das despesas no período analisado.
    *   Gráfico de linhas mostrando a evolução das despesas ao longo do tempo.
*   **Margem de Lucro:**
    *   Gráfico de linhas mostrando a evolução da margem de lucro ao longo do tempo.
    *   Cartão (KPI) mostrando a margem de lucro atual e a variação em relação ao período anterior.
*   **Total de Despesas por Componente:**
    *   Gráfico de barras mostrando a distribuição das despesas por componente.
*   **Total de Receitas por Componente:**
    *   Gráfico de barras mostrando a distribuição das receitas por componente.
*   **Principais Segmentos:**
    *   Gráfico de barras mostrando a receita ou lucro por segmento, destacando os principais.
    *   Tabela mostrando o desempenho de cada segmento
*   **Tabela por Período:**
    *   Tabela ou matriz mostrando as principais métricas (receitas, despesas, margem de lucro) para diferentes períodos (ex: mensal, trimestral, anual). Usando segmentações de dados (slicers) para filtrar os períodos desejados.

![Dashboard_Análise-financeira](https://github.com/user-attachments/assets/14fcb188-7f27-4387-bd07-5e895e63d4bb)

## Processo de ETL (Extração, Transformação e Carga)

1.  **Extração:** Os dados foram extraídos das fontes de dados usando o Power Query no Power BI Desktop.
2.  **Transformação:**
    *   Limpeza dos dados: tratamento de valores ausentes, remoção de duplicatas, etc.
    *   Criação de colunas calculadas:
        *   `Margem de Lucro = DIVIDE([Total de Receitas] - [Total de Despesas], [Total de Receitas])`
    *   Modelagem dos dados: criação de relações entre as tabelas, se necessário (ex: tabela de datas para análise temporal).
    *   Criação de medidas DAX (exemplos):
        *   `Total de Receitas = SUM(TabelaDeFinanças[Valor da receita])`
        *   `Total de Despesas = SUM(TabelaDeFinanças[Valor da despesa])`
        *   Medidas para calcular totais por componente e segmento, usando a função `CALCULATE`.
        *   Medidas para análise de variação entre períodos (ex: variação mês a mês, ano a ano).
3.  **Carga:** O modelo de dados foi carregado no Power BI Service para publicação e compartilhamento (opcional).

## Arquivo .pbix

O arquivo `Dashboard de Análise Financeira.pbix` contém o projeto completo do Power BI.

## Como visualizar

Para visualizar o dashboard interativamente, é necessário ter o Power BI Desktop instalado e abrir o arquivo `.pbix`. Para visualizar o dashboard online, acesse o link publicado no Power BI Service https://app.powerbi.com/groups/me/reports/b88c2952-ae07-44e7-bf26-df5521df7125?ctid=e5a2d57f-82e3-43da-af1c-1a2cc1b42330&pbi_source=linkShare.

## Contato

Auriane F Sousa - aurianef8@gmail.com
