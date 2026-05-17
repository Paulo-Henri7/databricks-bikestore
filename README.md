# 🚲Databricks Bikestore
Projeto de Engenharia de Dados desenvolvido no Databricks utilizando arquitetura medalhão (Bronze, Silver e Gold) para ingestão, transformação e disponibilização de dados analíticos com PySpark e SQL.

O projeto também conta com uma camada de observabilidade para monitoramento, rastreabilidade e análise das execuções das pipelines.

## 📖 Visão Geral

Este projeto implementa um pipeline de dados baseado na arquitetura medalhão utilizando Databricks, PySpark e SQL.

A solução contempla:
- Ingestão de dados brutos
- Transformação e padronização dos dados
- Criação de tabelas analíticas
- Monitoramento e rastreabilidade das pipelines
- Visualização de indicadores em dashboard 

## 🏗️Arquitetura do projeto

O projeto segue a arquitetura medalhão utilizando múltiplas camadas para organização e processamento dos dados.

### Landing
Camada responsável pelo armazenamento das fontes de dados brutas utilizadas no projeto.

### Bronze
Responsável pela ingestão inicial dos dados sem grandes transformações.

### Silver
Camada de tratamento, limpeza, padronização e aplicação das regras de negócio.

### Gold
Camada analítica otimizada para consultas, métricas e consumo analítico.

### Observability
Camada responsável pelo monitoramento das jobs, rastreamento das execuções e acompanhamento das métricas dos pipelines.
             
```text
Source Files
     ↓
  Bronze
     ↓
  Silver
     ↓
   Gold
     ↓
Destination
     ↓
 Dashboard

Observability:
logs • metrics • monitoring • jobs
```

## 📂 Estrutura do Projeto

```bash
bikestore/
│
├── landing/                        # dados de origem e entrega
│   ├── source/                     # arquivos CSV/Parquet recebidos da fonte
│   └── destination/                # exportações para dashboards e consumo analítico
│
├── bronze/                         # dados brutos (raw)
│   ├── brands/
│   ├── categories/
│   ├── customers/
│   ├── order_items/
│   ├── orders/
│   ├── products/
│   ├── staffs/
│   ├── stocks/
│   └── stores/
│
├── silver/                         # dados tratados e padronizados
│   ├── customers/
│   ├── orders/
│   └── products/
│
├── gold/                           # camada analítica
│   ├── orders_pending/
│   └── sales_ny/
│
└── observability/                  # monitoramento e métricas
    ├── data_quality_metrics/
    ├── ingestion_metrics/
    └── job_execution_metrics/
```


## ⚙️ Tecnologias Utilizadas

- Databricks
- PySpark
- Python
- SQL 
- Power BI
- Git/GitHub
