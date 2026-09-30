# Análise de RH - Equidade e Localização 📊
**Aluna:** Ana Maria Barbosa Dias  
**Turma:** Visualização de Dados e Business Intelligence - T3  

## 🎯 Objetivo do Trabalho
Este projeto tem como objetivo extrair e analisar informações de Recursos Humanos para apoiar a tomada de decisão estratégica corporativa. O foco analítico baseou-se na **equidade salarial e distribuição geográfica global**. O projeto foi estruturado em um formato de "Funil Analítico": partindo de uma visão macro (para identificar onde a força de trabalho está alocada e desmascarar vieses estatísticos de amostragem) até um "zoom" micro na sede da empresa (EUA), avaliando a verdadeira equidade salarial entre funcionários que exercem exatamente o mesmo cargo.

## 🗂️ Dicionário de Dados (Tabelas Utilizadas)
Os dados analisados representam as informações de RH de uma empresa multinacional que busca alinhar as suas práticas aos pilares ESG (Ambiental, Social e Governança). Para isso, o banco de dados Oracle foi explorado através das seguintes tabelas:
* **EMPLOYEES & JOBS:** Base principal com os funcionários, respectivos cargos e salários.
* **DEPARTMENTS:** Estrutura dos departamentos da empresa.
* **LOCATIONS, COUNTRIES & REGIONS:** Dados geográficos utilizados para o mapeamento da distribuição global de talentos.

## 🔍 Resumo das Consultas SQL
A extração de dados foi realizada através de consultas rigorosas utilizando `LEFT JOIN` e `INNER JOIN` para garantir a integridade dos relacionamentos:
1. **Consulta 01 (Visão Operacional Completa):** Extraiu-se toda a força de trabalho ativa utilizando o filtro `WHERE SALARY > 0`, unindo as tabelas `EMPLOYEES`, `DEPARTMENTS` e `JOBS`. O objetivo foi capturar o cenário real da empresa, sem excluir a base operacional.
2. **Consulta 02 (Mapeamento Geográfico):** Cruzou dados para mapear a localização exata (cidade, país e região) de toda a força de trabalho, permitindo a análise de concentração de talentos.

## 🐍 Análise Exploratória e Data Storytelling (Python)
Os arquivos CSV gerados pelo SQL foram importados para o **Google Colab** e analisados com **Pandas, Matplotlib e Seaborn**. 
* **Tratamento de Dados (EDA):** Identificou-se uma base de 107 registros globais, com a remoção de valores nulos e alinhamento de chaves para cruzamento exato no Python.
* **Visão Macro e o Viés de Amostragem:** A análise geográfica mostrou que a Alemanha possuía a maior média salarial global ($ 10.000). Contudo, a visualização gerada (Combo Chart) revelou um clássico **viés de amostragem**: a Alemanha possui apenas 1 funcionário em cargo de alto nível, enquanto os EUA concentram a real base operacional (68 funcionários).
* **Visão Micro (Auditoria de Equidade nos EUA):** Aplicou-se um filtro isolando a matriz (EUA) para comparar "maçãs com maçãs". O gráfico de disparidade salarial comprovou que, embora cargos executivos tenham alta equidade, a base técnica sofre com disparidades severas (ex: diferença de quase $ 5.000 entre profissionais no cargo de *Programmer*).

## 🚀 Como Executar o Projeto
1. Clone este repositório no seu ambiente local ou acesse os arquivos diretamente no GitHub.
2. Os scripts SQL (`consultas_rh.sql`) podem ser executados no **Oracle FreeSQL** ou ferramenta compatível (DBeaver/SQL Developer) utilizando o schema padrão `HR`.
3. Para visualizar a análise de dados e os gráficos, acesse o Google Colab e faça o upload do arquivo `analise_rh.ipynb` juntamente com os arquivos `query_01.csv` e `query_02.csv`.
4. Execute as células sequencialmente.

## 🔮 Sugestões de Melhoria para Futuras Versões
* **Ampliação do escopo de DE&I (Diversidade, Equidade e Inclusão):** Incluir dados demográficos (como gênero, idade e etnia) para cruzar com a variável de disparidade salarial encontrada nos cargos de TI, aprofundando a auditoria de equidade para entender se há desigualdade estrutural.
* **Dashboard Interativo:** Conectar as consultas SQL diretamente a uma ferramenta de BI (como Looker Studio ou Power BI) para que a Diretoria de RH possa monitorar o mapa de calor salarial em tempo real.
