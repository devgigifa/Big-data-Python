# Cosmic Census
### Classificação de Objetos Celestes com Big Data

Pipeline completo de Big Data sobre 100 mil observações reais do [Sloan Digital Sky Survey (SDSS DR17)](https://skyserver.sdss.org) para classificar objetos celestes em **estrelas**, **galáxias** e **quasares** usando PySpark, Pandas, Plotly e TensorFlow.

---

## Pergunta científica

> *"Dado um conjunto de medições fotométricas de um objeto no céu, ele é uma estrela, uma galáxia ou um quasar?"*

O modelo aprende a responder essa pergunta com **98% de acurácia** — sem que nenhuma regra seja programada manualmente. Os padrões são descobertos automaticamente a partir dos dados.

---

## Resultados

| Modelo | Acurácia |
|---|---|
| Random Forest (Scikit-learn) | **98.03%** |
| Rede Neural MLP (TensorFlow) | **97.68%** |
| Pipeline Distribuído (Spark MLlib) | **97.30%** |

---

## Tecnologias

| Camada | Tecnologia |
|---|---|
| Processamento distribuído | Apache Spark 4 (PySpark) |
| Data Lake | Parquet (compressão Snappy) |
| Análise exploratória | Pandas + Plotly (gráficos interativos) |
| Machine Learning | Scikit-learn Random Forest |
| Deep Learning | TensorFlow / Keras MLP |
| Pipeline escalável | Spark MLlib |
| Linguagem | Python 3.10+ |

---

## Como executar

### Google Colab (recomendado — sem instalação)
1. Acesse [colab.research.google.com](https://colab.research.google.com)
2. Clique em **Arquivo → Fazer upload de notebook** e envie `cosmic_census.ipynb`
3. Execute a célula 0 (instala as dependências automaticamente)
4. Execute as demais células em ordem com **Runtime → Run all**

### Localmente (VSCode ou Jupyter)
Pré-requisitos: Python 3.10+, Java 8 ou 11 (obrigatório para o Spark)

```bash
pip install -r requirements.txt
jupyter notebook cosmic_census.ipynb
```

---

## Pipeline

```
[SDSS CSV]  →  [Data Lake Parquet]  →  [PySpark: limpeza + features]
    →  [Pandas: EDA + Plotly]  →  [TensorFlow: classificação]
    →  [Avaliação + Spark MLlib Pipeline]
```

---

## Conteúdos cobertos

| Módulo | O que é aplicado |
|---|---|
| Princípios de Big Data | Os 5 Vs, ecossistema, data lake |
| Hadoop e armazenamento | HDFS vs RDBMS, Parquet como Data Lake |
| PySpark | SparkSession, RDDs, DataFrames, MapReduce |
| Pandas + Plotly | EDA completa, 5 visualizações interativas |
| Big Data Analytics | KDD pipeline, Random Forest, rede neural |

---

## Dataset

- **Fonte:** [Sloan Digital Sky Survey DR17](https://skyserver.sdss.org)
- **Tamanho:** 100.000 observações × 18 features
- **Classes:** GALAXY (59.4%), STAR (21.6%), QSO/Quasar (19%)
- **Licença:** Domínio público (SDSS)

---

*Projeto de portfólio — Tópicos de Big Data em Python · Engenharia da Computação*
