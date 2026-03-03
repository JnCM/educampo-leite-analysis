# Análise de Produção de Leite - Educampo/SEBRAE/UFV

Este repositório contém as análises e modelos de Machine Learning desenvolvidos para predizer o comportamento da produção de leite e custos associados em diferentes fazendas e sistemas de produção ao longo dos anos. O projeto é realizado em parceria com o **SEBRAE (Projeto Educampo)** e a **Universidade Federal de Viçosa (UFV)**.

## 📌 Sobre o Projeto

O objetivo principal é aplicar técnicas de ciência de dados para transformar dados brutos de produção leiteira em insights preditivos, auxiliando na gestão de fazendas e na compreensão de fatores que impactam a produtividade e a rentabilidade do setor.

## 📂 Estrutura do Repositório

O projeto está organizado da seguinte forma:

* **`FormatacaoDados.ipynb`**: Notebook dedicado ao pipeline de limpeza, tratamento e preparação dos dados brutos (ETL).
* **`TesteModelagem - Producao.ipynb`**: Experimentos e validação de modelos de regressão/séries temporais voltados para a **predição de volume de produção**.
* **`TesteModelagem - Custo.ipynb`**: Modelagem focada na análise e predição dos **custos de produção**.
* **`resultados/`**: Pasta contendo os outputs, gráficos e métricas geradas pelos modelos.

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Python
* **Ambiente:** Jupyter Notebook
* **Principais Bibliotecas:**
* `pandas` e `numpy` para manipulação de dados.
* `scikit-learn` para implementação de algoritmos de Machine Learning.
* `statsmodels` para análise de features.



## 🚀 Como Utilizar

1. **Clone o repositório:**
```bash
git clone https://github.com/JnCM/educampo-leite-analysis.git

```


2. **Instale as dependências:**
Certifique-se de ter o Python instalado. Recomenda-se o uso de um ambiente virtual:
```bash
pip install -r requirements.txt

```


3. **Execução:**
Inicie o Jupyter Notebook para visualizar as análises:
```bash
jupyter notebook

```


Siga a ordem lógica: primeiro execute o `FormatacaoDados.ipynb` para preparar os dados e depois os notebooks de modelagem.

## 📊 Resultados

Os modelos buscam identificar padrões sazonais e tendências econômicas que afetam o setor leiteiro, permitindo uma tomada de decisão baseada em dados para os produtores do projeto Educampo.

## 👥 Contribuição

Este é um projeto acadêmico/profissional. Sinta-se à vontade para abrir uma *issue* ou enviar um *pull request* com melhorias.

---

**Desenvolvido por:** [Josué Campos (JnCM)](https://github.com/JnCM)

**Instituição:** UFV / SEBRAE - Projeto Educampo