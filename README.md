# Data Sanitization Pipeline (Python Nativo)

Este projeto consiste na construção de um pipeline de Engenharia de Dados focado na limpeza, padronização e sanitização de dados.

O objetivo é demonstrar domínio da linguagem Python, usando exclusivamente bibliotecas nativas como csv, re, datetime, operadores padrões e aplicação de regras de negócio para construir um pipeline de sanitização.

---

# Pipeline de Sanitização de Dados (Python Nativo)

## Descrição do Projeto
Este projeto foi desenvolvido para solucionar problemas de inconsistência e sujeira em dados reais de e-commerce da **Olist**. Frequentemente, bases de dados brutas chegam com valores nulos, formatos de datas incorretos, caracteres especiais indesejados e registros corrompidos que inviabilizam análises precisas ou a construção de modelos preditivos confiáveis.

O objetivo deste script é construir um **Pipeline de Engenharia de Dados (ETL)** totalmente automatizado para limpar, padronizar e higienizar dois datasets fundamentais (`produtos` e `pedidos`). O grande diferencial técnico é que todo o processamento foi construído **exclusivamente com bibliotecas nativas do Python** (`csv`, `re` e `datetime`), sem o uso de bilbiotecas como o *Pandas*.

---

## Guia de Execução

Siga os passos abaixo para testar o pipeline no seu próprio ambiente:

### 1. Preparação dos Arquivos
Faça o download dos arquivos de dados brutos e garanta que eles estejam salvos com os seguintes nomes no mesmo diretório do script:
* `dataset_produtos.csv`
* `dataset_pedidos.csv`

Obs: Para testar este código, baixe os arquivos CSV deste repositório e faça o upload deles no seu ambiente Colab ou pasta local.


### 2. Execução do Script
1. Clone este repositório.
2. Certifique-se de ter os arquivos `dataset_produtos.csv` e `dataset_pedidos.csv` no mesmo diretório.
3. Lembre-se de alterar o caminho dos arquivos para o seu ambiente Colab ou pasta local.
4. Execute o script principal.

### 3. Resultados
Ao final da execução, o console exibirá um relatório estatístico e o script irá gerar automaticamente os arquivos perfeitamente higienizados no seu diretório.


## Reflexão Teórica: O Papel da Limpeza de Dados no Machine Learning

A lógica de programação aplicada à higienização rigorosa dos dados não é apenas uma questão de organização estética, ela é o alicerce fundamental para a construção de modelos de Inteligência Artificial confiáveis. Em Machine Learning, vigora a regra máxima do **"Garbage In, Garbage Out"** (Lixo entra, lixo sai). Quando deixamos categorias de produtos vazias ou poluídas com caracteres especiais, o algoritmo entende erroneamente que se tratam de entidades diferentes. Isso dilui a relevância das variáveis e pode gerar algum viés, onde o modelo favorece padrões inexistentes gerados por pura formatação inconsistente.

Além disso, a limpeza correta ajuda a mitigar o risco de **Overfitting** ou **Underfitting**. Se um modelo treina com dados nulos, datas corrompidas ou produtos sem dimensões físicas, ele usará essas exceções como se fossem regras de negócio válidas, o que pode acarretar em uma estimativa muito acima ou muito abaixo do valor real. Ao aplicarmos regras de negócio rigorosas via pipeline, como o descarte de produtos sem dimensão ou a padronização via Regex, nós entregamos ao modelo um sinal claro e padronizado. Um dado bem tratado permite que o algoritmo generalize melhor, aprendendo o comportamento real do consumidor da Olist.
