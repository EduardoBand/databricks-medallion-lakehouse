# Data Lakehouse: Sales Pipeline with Medallion Architecture 

![Databricks](https://img.shields.io/badge/Databricks-FF6F00?style=flat&logo=databricks) 
![PySpark](https://img.shields.io/badge/PySpark-EE4C2C?style=flat&logo=apache-spark) 
![Delta Lake](https://img.shields.io/badge/Delta%20Lake-3F51B5?style=flat&logo=delta-lake) 
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python)

Este repositório apresenta um **pipeline completo de Data Engineering** no **Databricks**, usando **PySpark** e **Delta Lake**.  
O projeto implementa a arquitetura **Medallion (Bronze, Silver e Gold)** para processar, transformar e otimizar dados de vendas para análise e BI.

---

## 🎯 Objetivos do Projeto
- Construir um pipeline **end-to-end** de dados de vendas.  
- Aplicar o conceito de **Medallion Architecture**.  
- Garantir **qualidade, rastreabilidade e eficiência** no processamento de dados.  
- Entregar tabelas prontas para análises e dashboards.

---

## 🏗️ Arquitetura do Pipeline

**Fluxo de dados:**

Landing Zone → Bronze Layer → Silver Layer → Gold Layer → BI / Analytics

- **Landing Zone**: Ingestão de dados brutos de fontes externas.  
- **Bronze Layer**: Armazena dados brutos em **Delta Lake** para auditoria e histórico.  
- **Silver Layer**: Limpeza, tratamento de nulos, validação de schema e enriquecimento.  
- **Gold Layer**: Tabelas modeladas em **Star Schema** (Fatos e Dimensões) otimizadas para BI.

---

## 📁 Estrutura do Repositório

| Notebook | Descrição |
|----------|-----------|
| `000 Setup DBFS` | Configuração inicial e montagem de diretórios. |
| `001 Import Data` | Ingestão automatizada para a Landing Zone. |
| `002 Load Bronze` | Carga inicial de dados brutos em Delta. |
| `003 Silver Transformation` | Limpeza, cast de tipos e transformações intermediárias. |
| `004 Load Gold Delta` | Modelagem dimensional com **Surrogate Keys**. |
| `005 Incremental Gold Load` | Processamento incremental para eficiência. |
| `006 Optimized Queries` | Exemplos de queries SQL/Spark otimizadas. |
| `007 Delta Table Creation` | Registro das tabelas no **Hive Metastore / Unity Catalog**. |
| `008 Delta Maintenance` | Governança: `VACUUM`, `OPTIMIZE`, **Z-Ordering**. |

---

## 🛠️ Tecnologias & Recursos

- **PySpark**: Processamento distribuído.  
- **Delta Lake**: ACID, Time Travel e versionamento.  
- **Star Schema**: Estrutura otimizada para análise.  
- **Performance**: Z-Ordering, Optimize, Vacuum.  
- **Memória**: `gc.collect()`, `unpersist()`, configuração Spark.

---

## 🚀 Como Executar

1. Crie um workspace no **[Databricks](https://databricks.com/)**.  
2. Importe os notebooks da pasta `/notebooks`.  
3. Execute na **ordem numérica**.  
4. Configure um cluster Spark compatível com **Delta Lake** OU utilize o serviço Serveless da Free Edition.
5. *Caso você tenha a versão standard (ou +), você poderá utilizar esses notebooks para gerar um Workflow do processo.*
6. Totalmente usavel em PowerBI.
---

## 🔗 Links Úteis
- [Documentação PySpark](https://spark.apache.org/docs/latest/api/python/)  
- [Delta Lake Docs](https://delta.io/)  
- [Databricks Free Edition](https://community.cloud.databricks.com/)  

---

✨ Este projeto segue as melhores práticas de **Data Engineering**, fornecendo um pipeline **escalável, eficiente e pronto para análises de vendas**.
