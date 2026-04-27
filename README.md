# Democracia liberal no Brasil e nos EUA com dados V-Dem

Este repositório reúne scripts em R para replicar gráficos e tabelas sobre a média do índice de democracia liberal do V-Dem (`v2x_libdem`) por governo, entre 1988 e 2025, para Brasil e Estados Unidos.

## Objetivo

O objetivo é organizar uma rotina simples e replicável para:

1. carregar os dados do pacote `vdemdata`;
2. filtrar Brasil e Estados Unidos no período de 1988 a 2025;
3. classificar os anos por governo;
4. calcular a média do índice de democracia liberal por governo;
5. gerar gráficos prontos para análise e divulgação.

## Scripts

### `R/00_setup.R`

Instala e carrega os pacotes necessários para a replicação.

### `R/01_brasil_vdem.R`

Produz a tabela e o gráfico da média do índice de democracia liberal no Brasil por governo.

Saídas esperadas:

- `data_output/brasil_media_vdem_por_governo.csv`
- `figures/brasil_democracia_liberal_por_governo.png`

### `R/02_eua_vdem.R`

Produz a tabela e o gráfico da média do índice de democracia liberal nos Estados Unidos por governo.

Saídas esperadas:

- `data_output/eua_media_vdem_por_governo.csv`
- `figures/eua_democracia_liberal_por_governo.png`

### `R/03_comparativo_brasil_eua.R`

Reúne as tabelas de Brasil e Estados Unidos em um único arquivo comparativo.

Saída esperada:

- `data_output/comparativo_brasil_eua_vdem.csv`

## Como replicar

Abra o projeto no RStudio e execute os scripts nesta ordem:

```r
source("R/00_setup.R")
source("R/01_brasil_vdem.R")
source("R/02_eua_vdem.R")
source("R/03_comparativo_brasil_eua.R")
```

## Fonte dos dados

Os dados são provenientes do projeto V-Dem, acessados por meio do pacote `vdemdata` no R.

Variável utilizada:

- `v2x_libdem`: índice de democracia liberal.

## Observação metodológica

As médias por governo são descritivas. Elas sintetizam o comportamento médio do índice em cada período presidencial, mas não devem ser interpretadas como estimativas causais do efeito de cada governo sobre a democracia liberal. A comparação é útil como descrição histórica e como ponto de partida para análises mais aprofundadas.
