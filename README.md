# **Carteira de Ativos - Análise de Performance**

Este repositório contém um script Python para analisar a performance de uma carteira de ativos financeiros, comparando a evolução das cotações de cada ativo e do índice Ibovespa.

## **Requisitos**

- Python 3
- Bibliotecas:
    - numpy
    - pandas
    - matplotlib
    - pandas_datareader
    - yfinance

## **Instruções de uso**

1. Clone este repositório.
2. Crie um arquivo chamado **`carteira.xlsx`** com os ativos da carteira e suas respectivas quantidades, conforme o exemplo abaixo:

| Ativos | Tipo | Qtde |
| --- | --- | --- |
| BOVA11 | ETF | 100 |
| SMAL11 | ETF | 100 |
| MGLU3 | Ação | 1000 |
| ... | ... | ... |
1. Execute o script **`main.py`** para gerar a análise gráfica da performance da carteira.

## **Funcionalidades**

O script realiza as seguintes etapas:

1. Importa os dados da carteira do arquivo **`carteira.xlsx`**.
2. Obtém as cotações históricas dos ativos da carteira, utilizando as bibliotecas **`pandas_datareader`** e **`yfinance`**.
3. Trata os dados faltantes (caso haja algum ativo com dados incompletos).
4. Normaliza os dados de cotação para comparação da performance individual dos ativos.
5. Plota um gráfico da performance da carteira de ativos.
6. Obtém as cotações históricas do índice Ibovespa, para comparação com a performance da carteira.
7. Cria um dataframe com o valor investido em cada ativo, considerando a quantidade de ações na carteira.
8. Calcula e plota o gráfico do valor total da carteira ao longo do tempo.
9. Plota um gráfico comparativo entre a performance da carteira e do índice Ibovespa.

## **Limitações**

- Os dados de cotação estão limitados ao período entre 2020-01-01 e 2020-11-10.
- O script não suporta ações que foram deslistadas ou tiveram seus tickers alterados.
- O script não considera dividendos, juros sobre capital próprio ou outras operações financeiras que possam impactar o valor da carteira.
- Os dados do índice Ibovespa são utilizados apenas como referência e não representam a performance de um investimento real.
