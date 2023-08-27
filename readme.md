# ETL de Dados do Tesouro Direto

Este é um script Python que realiza um processo de ETL (Extração, Transformação e Carga) em dados do Tesouro Direto disponibilizados pelo Governo Brasileiro.

## Descrição

O script tem como objetivo extrair dados de vendas e preços/taxas do Tesouro Direto, realizar ajustes necessários nos valores, transformar as datas em objetos datetime e, finalmente, persistir os dados em arquivos CSV.

## Requisitos

- Python 3.x
- Bibliotecas Python: pandas

## Como Usar

1. Certifique-se de que você tenha o Python instalado em seu sistema.
2. Instale a biblioteca pandas, caso ainda não a tenha, utilizando o seguinte comando:
3. Execute o script `etl_tesouro_direto.py` em seu ambiente Python.

## Ajustes de Separador Decimal

O script inclui uma função chamada `ajusta_separador(valor)` que ajusta o separador de valores decimais de vírgula para ponto. Essa função é aplicada às colunas especificadas nos dataframes para garantir a consistência dos valores.

## Transformação de Datas

As datas presentes nos dataframes são transformadas em objetos datetime utilizando a função `pd.to_datetime()`. 

## Persistência dos Dados

Os dataframes resultantes após a etapa de transformação são salvos em arquivos CSV. Isso permite que os dados processados sejam reutilizados ou compartilhados com outras aplicações.

## Fontes de Dados

- Vendas Tesouro Direto: [Link para o CSV](https://www.tesourotransparente.gov.br/ckan/dataset/f0468ecc-ae97-4287-89c2-6d8139fb4343/resource/e5f90e3a-8f8d-4895-9c56-4bb2f7877920/download/VendasTesouroDireto.csv)
- Preço/Taxa Tesouro Direto: [Link para o CSV](https://www.tesourotransparente.gov.br/ckan/dataset/df56aa42-484a-4a59-8184-7676580c81e3/resource/796d2059-14e9-44e3-80c9-2d9e30b405c1/download/PrecoTaxaTesouroDireto.csv)

Obs: Uma cópia dos dados em bruto, extraídos em 26/08/2023 foi salva, para o caso da página ficar indisponível.
