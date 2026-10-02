# 📊 Análise de RH — Equidade Salarial e Localização

Projeto de análise de dados de Recursos Humanos desenvolvido para investigar **disparidades salariais e distribuição geográfica de funcionários**, utilizando SQL e Python.

A análise foi estruturada em um **Funil Analítico**: parte-se de uma visão macro da distribuição global dos funcionários para investigar possíveis vieses de amostragem e, posteriormente, realiza-se um recorte mais detalhado da sede da empresa nos Estados Unidos para analisar diferenças salariais entre departamentos e cargos.

---

## 📌 Índice

* [Sobre o projeto](#sobre-o-projeto)
* [Tecnologias utilizadas](#tecnologias-utilizadas)
* [Estrutura do projeto](#estrutura-do-projeto)
* [Como executar](#como-executar)
* [Resultados e análise](#resultados-e-análise)
* [Apresentação executiva](#apresentação-executiva)
* [Contribuições](#contribuições)

---

## 🔎 Sobre o projeto

O objetivo deste projeto é extrair, tratar e analisar informações de Recursos Humanos para apoiar a **tomada de decisão baseada em dados**, com foco em:

* distribuição geográfica da força de trabalho;
* representatividade das localidades na amostra;
* distribuição salarial;
* diferenças salariais entre departamentos e cargos;
* identificação de possíveis disparidades que mereçam investigação adicional.

Os dados foram extraídos de um banco de dados **Oracle**, a partir de tabelas relacionadas a funcionários, departamentos e localizações, utilizando consultas relacionais com `JOINs`.

Posteriormente, os dados foram processados e visualizados em **Google Colab**, utilizando Python e bibliotecas de análise e visualização de dados.

### 🎯 Abordagem analítica

A análise segue uma lógica de **funil**:

**Visão global → Distribuição geográfica → Identificação de possíveis vieses → Recorte da sede nos EUA → Análise salarial por departamento e cargo**

Essa abordagem permite contextualizar os resultados salariais antes de realizar análises mais específicas.

---

## 🛠️ Tecnologias utilizadas

### Banco de dados

* Oracle FreeSQL
* DBeaver ou SQL Developer

### Linguagem

* Python
* SQL

### Bibliotecas Python

* Pandas
* Matplotlib
* Seaborn

### Ambiente

* Google Colab
* Jupyter Notebook

---

## 📁 Estrutura do projeto

```text
projeto-avaliativo-Mod1-Modelagem_dados/
│
├── consultas_rh.sql
├── analise_rh.ipynb
├── query_01.csv
├── query_02.csv
├── CONTRIBUTING.md
└── README.md
```

---

## 🚀 Como executar

### 1. Clone o repositório

```bash
git clone https://github.com/Engineer-Ana/projeto-avaliativo-Mod1-Modelagem_dados.git
```

### 2. Extraia os dados utilizando SQL

Execute os scripts disponíveis em:

```text
consultas_rh.sql
```

no seu gerenciador de banco de dados Oracle.

As consultas devem gerar os arquivos:

```text
query_01.csv
query_02.csv
```

### 3. Execute a análise em Python

Abra o notebook:

```text
analise_rh.ipynb
```

no Google Colab ou em um ambiente Jupyter Notebook.

Faça o upload dos arquivos:

```text
query_01.csv
query_02.csv
```

e execute as células sequencialmente.

O notebook realiza os cálculos estatísticos e gera as visualizações utilizadas na análise.

---

## 📈 Resultados e análise

A análise produz, entre outros resultados:

* distribuição de funcionários por localização;
* comparação entre quantidade de funcionários e remuneração;
* análise salarial por departamento;
* análise salarial por cargo;
* identificação de possíveis disparidades salariais;
* visualizações para investigação de possíveis vieses de amostragem.

Os resultados devem ser interpretados considerando o **recorte da base analisada** e não necessariamente representam a totalidade da força de trabalho da organização.

---

## 📺 Apresentação executiva

Para acompanhar os principais insights obtidos na análise e entender as conclusões apresentadas a partir das visualizações, consulte a apresentação executiva do projeto:

**[▶️ Assistir à Apresentação do Projeto](https://drive.google.com/file/d/1U0onDsidRhNYCLkCv4mj-R5WdlfJaOke/view?usp=sharing)**

---

## 🤝 Contribuições

Contribuições são bem-vindas.

Consulte o arquivo [`CONTRIBUTING.md`](../CONTRIBUTING.md) para obter informações sobre o código de conduta e o processo para envio de *pull requests*.

---

## 📄 Licença

Caso o projeto possua uma licença específica, ela deve ser indicada aqui.

---
