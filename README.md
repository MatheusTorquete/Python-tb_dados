
# Análise de Dados com Python no Google Colab

Este projeto envolve a análise de dados utilizando a linguagem de programação Python no ambiente do Google Colab. O conjunto de dados utilizado é o "tb_dados.csv", que contém informações sobre filmes e séries, incluindo detalhes como tipo, título, ano de lançamento, avaliação, quantidade de avaliações, duração, etc.

## Passo 1: Importação e Visualização dos Dados

```python
import pandas as pd

# Importando os dados do arquivo CSV para um DataFrame
df = pd.read_csv("tb_dados.csv", delimiter=";", encoding='latin-1', error_bad_lines=False)

# Visualizando as primeiras 20 linhas do DataFrame
print("Visualizando os 20 Primeiros")
print(df.head(20))
```

Neste passo, os dados foram importados para um DataFrame e as primeiras 20 linhas foram visualizadas.

## Passo 2: Manipulação e Análise dos Dados

### 2.1 Imprimindo o valor da segunda linha da primeira coluna

```python
# Imprimindo o valor da segunda linha da primeira coluna
print("Valor da segunda linha da primeira coluna:")
print(df.iloc[1, 0])
```

### 2.2 Selecionando a segunda linha e a segunda coluna do DataFrame

```python
# Selecionando a segunda linha e a segunda coluna do DataFrame
segunda_linha_segunda_coluna = df.iloc[1, 1]
print("Segunda linha, segunda coluna:")
print(segunda_linha_segunda_coluna)
```

### 2.3 Encontrando o filme com a avaliação mais alta

```python
# Encontrando o filme com a avaliação mais alta
filme_mais_avaliado = df[df['avaliacoes_qtd'] == df['avaliacoes_qtd'].max()]
print("Filme com a avaliação mais alta:")
print(filme_mais_avaliado)
```

### 2.4 Removendo a coluna "Id diretor"

```python
# Removendo a coluna "Id diretor"
df = df.drop(columns=["Id_diretor"])
```

### 2.5 Renomeando a coluna "Id_avaliacao" para "Cod_avaliacao"

```python
# Renomeando a coluna "Id_avaliacao" para "Cod_avaliacao"
df = df.rename(columns={"Id_avaliacao": "Cod_avaliacao"})
```
