# Databricks Bikestore
Projeto de dados desenvolvido com arquitetura medalhão (Bronze, Silver e Gold), aplicando ingestão e transformação de dados em PySpark e SQL, juntamente com uma camada de observabilidade para monitoramento e análise das execuções das jobs.

## 📖 Visão Geral

Este projeto implementa um pipeline de dados baseado na arquitetura medalhão utilizando Databricks, PySpark e SQL.

A solução contempla:
- Ingestão de dados brutos
- Transformação e padronização dos dados
- Criação de tabelas analíticas
- Monitoramento das pipelines
- Visualização de indicadores em dashboard 

## Arquitetura do projeto

O projeto segue a arquitetura medalhão utilizando múltiplas camadas para organização e processamento dos dados.

### Landing
Camada responsável pelo armazenamento das fontes de dados brutas utilizadas no projeto.

### Bronze
Responsável pela ingestão inicial dos dados sem grandes transformações.

### Silver
Camada de tratamento, limpeza, padronização e aplicação das regras de negócio.

### Gold
Camada analítica otimizada para consultas, métricas e consumo em dashboards.

### Observability
Camada responsável pelo monitoramento das jobs, rastreamento das execuções e acompanhamento das métricas dos pipelines.
             
Source Files --> Bronze --> Silver --> Gold --> Destination --> Dashboard
             
Observability (logs, metrics, monitoring, jobs)

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
