# Análise de RH - Equidade e Localização 📊
**Aluna:** Ana Maria Barbosa Dias  
**Turma:** Visualização de Dados e Business Intelligence - T3  

## 🎯 Objetivo do Trabalho
Este projeto tem como objetivo extrair e analisar informações de Recursos Humanos para apoiar a tomada de decisão estratégica. O foco analítico baseou-se na **equidade salarial e distribuição geográfica**. Foram estabelecidos pontos de corte e cruzamentos de dados por país para identificar discrepâncias e entender como a remuneração se comporta em diferentes regiões, fornecendo insights valiosos para políticas de retenção e justiça corporativa (ESG).

## 🗂️ Dicionário de Dados (Tabelas Utilizadas)
Os dados analisados representam as informações de Recursos Humanos de uma empresa multinacional que busca alinhar as suas práticas aos conceitos de ESG e equidade. Para isso, o banco de dados Oracle foi explorado através das seguintes tabelas:
* **EMPLOYEES & JOBS:** Base principal com os funcionários, respectivos cargos e salários.
* **DEPARTMENTS:** Estrutura dos departamentos da empresa.
* **LOCATIONS, COUNTRIES & REGIONS:** Dados geográficos utilizados para o mapeamento da distribuição global de talentos.

## 🔍 Resumo das Consultas SQL
A extração de dados foi realizada através de duas consultas principais utilizando `LEFT JOIN` para garantir a integridade dos relacionamentos:
1. **Consulta 01 (Filtro Tático):** Identificou funcionários com salários superiores a 5.000, unindo as tabelas `EMPLOYEES`, `DEPARTMENTS` e `JOBS`. O objetivo foi isolar a faixa salarial de especialistas e gestores para análise de cargos.
2. **Consulta 02 (Mapeamento Geográfico):** Cruzou dados de `EMPLOYEES`, `DEPARTMENTS`, `LOCATIONS`, `COUNTRIES` e `REGIONS` para mapear a localização exata (cidade, país e região) de toda a força de trabalho, permitindo a análise de equidade global.

## 🐍 Análise Exploratória com Python
Os arquivos CSV gerados pelo SQL foram importados para o **Google Colab** e analisados com a biblioteca **Pandas**. 
* **Estatística Descritiva:** Calculou-se a Média (6.456,75) e a Mediana (6.150,00) globais. A proximidade entre os valores indica uma distribuição salarial simétrica, sem presença de *outliers* extremos (super salários) que distorçam a realidade da folha de pagamento.
* **Visualização:** Foi aplicado o método `groupby` para agregar os salários por país, gerando um gráfico de barras que facilitou a rápida identificação das discrepâncias regionais.

## 🚀 Como Executar o Projeto
1. Clone este repositório no seu ambiente local.
2. Os scripts SQL (`consultas_rh.sql`) podem ser executados no **Oracle FreeSQL** ou ferramenta compatível (DBeaver/SQL Developer) utilizando o schema padrão `HR`.
3. Para visualizar a análise de dados, acesse o Google Colab, faça o upload do arquivo `analise_rh.ipynb` juntamente com os arquivos `query_01.csv` e `query_02.csv`.
4. Execute as células sequencialmente para reproduzir os cálculos e os gráficos.

## 🔮 Sugestões de Melhoria para Futuras Versões
* **Ampliação do escopo de DE&I:** Incluir dados demográficos (como gênero e idade, caso disponíveis) para cruzar com a variável de salário e região, aprofundando a auditoria de equidade.
* **Dashboard Interativo:** Conectar as consultas SQL diretamente a uma ferramenta de BI (como Looker Studio ou Power BI) para que a Diretoria de RH possa monitorar a equidade salarial em tempo real.
