# Dashboard de Performance de Marketing & Growth
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![Google BigQuery](https://img.shields.io/badge/Google_BigQuery-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-00758F?style=for-the-badge&logo=sqlite&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=for-the-badge&logo=dbt&logoColor=white)


## Visão Geral do Projeto
Este projeto consiste no desenvolvimento de um dashboard analítico de para monitoramento de KPIs estratégicos de Marketing. O objetivo principal foi centralizar dados de múltiplos canais de mídida (meta, google, bing e orgânico) juntando com dados de lead e opportunity (salesforce), garantindo uma única fonte da verdade para a tomada de decisão da área responsável.

> **Nota de Compliance:** Por questões de confidencialidade e segurança (LGPD/Segredo de Negócio), todos os dados numéricos, nomes de campanhas reais e valores financeiros foram omitidos. O foco deste repositório é demonstrar a arquitetura técnica, modelagem de dados e design da solução.

---

## Arquitetura e Engenharia de Dados (ELT)
A solução foi desenhada utilizando a estrutura já desenhada do pipeline de dados:

1. **Ingestão (Bronze):** Dados brutos extraídos de plataformas de tráfego/CRM (Salesforce, Google Ads, Meta Ads) e consolidados no Data Warehouse.
2. **Transformação & Modelagem (Prata/Ouro):** Utilização do **dbt (Data Build Tool)** e **SQL Avançado** dentro do **Google Cloud Platform (BigQuery)**.
   - Aplicação de boas práticas de modelagem dimensional (Star Schema).
   - Criação de tabelas Fato de mídias e Fato do salesforce, já existente no caso do salesforce, sendo feito pequenos ajustes.

---

## KPIs Consolidados e Visualização de Dados (Power BI)
Criado dentro do POWERBI os joins e dimensões entre as tabelas, e KPIs tradicionais de marketing, com isso facilitando o uso por parte da área de negócio e mantendo padrão star schema. Principais KPIs criadas:

A interface gráfica foi construída no **Microsoft Power BI** focando em UX (User Experience) e Storytelling:

* **CAC (CTR):** Proporção de clicks em relação ao total de impressões.
* **CPC:** Custo por clicks.
* **CPM:** Custo por cada mil impressões.
* **Perc WL:** De acordo com regras internas, relação entre leads e workable leads.
* **CPL:** Custo por lead.
* **CPwL:** Custo por workable lead.
* **CPS:** Custo por sale.

Visuais com linhas com mais de um eixo Y (Comparar KPIs com valores de métricas diferentes), mapa de calor (analisar dia da semana), gráifco de dispersão (comparar 3 variáveis num gráfico só) são exemplos de uso consciente de gráficos.

---

## Tecnologias Utilizadas
* **Google BigQuery** (Data Warehouse & SQL Engine)
* **dbt (Data Build Tool)** (Transformação, documentação e linhagem de dados)
* **Microsoft Power BI** (Visualização e DAX)
* **Git/GitHub** (Versionamento de código)
