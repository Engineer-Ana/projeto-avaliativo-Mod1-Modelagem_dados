# Análise de RH - Equidade e Localização 📊

## Índice
+ [Sobre](#sobre)
+ [Começando](#comecando)
+ [Uso](#uso)
+ [Contribuições](../CONTRIBUTING.md)

## Sobre <a name="sobre"></a>
Este projeto tem como objetivo extrair e analisar informações de Recursos Humanos para apoiar a tomada de decisão estratégica corporativa, com foco na **equidade salarial e distribuição geográfica global**. O projeto foi estruturado em um formato de "Funil Analítico": partindo de uma visão macro (para identificar viés de amostragem na alocação global) até um "zoom" micro na sede da empresa (EUA), avaliando a verdadeira equidade salarial.

Os dados foram extraídos de um banco de dados Oracle (tabelas de funcionários, departamentos e localizações) utilizando consultas relacionais complexas (`JOIN`s) e, posteriormente, processados e visualizados no Google Colab utilizando as bibliotecas Pandas, Matplotlib e Seaborn do Python.

## Começando <a name="comecando"></a>
Estas instruções guiarão você para obter uma cópia do projeto e executá-lo na sua máquina local para fins de teste e desenvolvimento.

### Pré-requisitos
Para reproduzir esta análise, você precisará das seguintes ferramentas:
* **Banco de Dados:** Oracle FreeSQL, DBeaver ou SQL Developer.
* **Ambiente Python:** Google Colab ou Jupyter Notebook local.
* **Bibliotecas Python:** `pandas`, `matplotlib`, `seaborn`.

### Instalação e Execução
Siga este passo a passo para reproduzir o ambiente de desenvolvimento:

1. **Clone o repositório:**
```bash
git clone https://github.com/Engineer-Ana/projeto-avaliativo-Mod1-Modelagem_dados.git
Extração dos Dados (SQL):
Execute os scripts localizados em consultas_rh.sql no seu gerenciador de banco de dados para exportar os arquivos query_01.csv e query_02.csv.
´´´

### Análise de Dados (Python):
Faça o upload do notebook analise_rh.ipynb e dos arquivos CSV gerados para o seu ambiente do Google Colab.
Execute todas as células sequencialmente para gerar os cálculos estatísticos, os gráficos de disparidade salarial e a prova do viés de amostragem.

### Uso 
Os resultados e gráficos desta análise destinam-se a auditorias internas de RH e comitês de Diversidade, Equidade e Inclusão (DE&I).

### 📺 Apresentação Executiva (Vídeo):
Para entender os insights gerados e as conclusões tomadas a partir dos gráficos (como o Combo Chart de distribuição x salário), assista ao resumo executivo abaixo:
Assistir à Apresentação do Projeto
https://drive.google.com/file/d/1U0onDsidRhNYCLkCv4mj-R5WdlfJaOke/view?usp=sharing
Contribuições
Consulte CONTRIBUTING.md para obter detalhes sobre o nosso código de conduta e o processo para nos enviar pull requests.


