# Cosmic Census
### Celestial Object Classification with Big Data

A complete Big Data pipeline over 100,000 real observations from the [Sloan Digital Sky Survey (SDSS DR17)](https://skyserver.sdss.org) to classify celestial objects as **stars**, **galaxies**, or **quasars** using PySpark, Pandas, Plotly, and TensorFlow.

---

## Scientific question

> *"Given a set of photometric measurements of an object in the sky, is it a star, a galaxy, or a quasar?"*

The model learns to answer this question with **98% accuracy** — without any manually programmed rules. Patterns are discovered automatically from the data.

---

## Results

| Model | Accuracy |
|---|---|
| Random Forest (Scikit-learn) | **98.03%** |
| Neural Network MLP (TensorFlow) | **97.68%** |
| Distributed Pipeline (Spark MLlib) | **97.30%** |

---

## Tech stack

| Layer | Technology |
|---|---|
| Distributed processing | Apache Spark 4 (PySpark) |
| Data Lake | Parquet (Snappy compression) |
| Exploratory analysis | Pandas + Plotly (interactive charts) |
| Machine Learning | Scikit-learn Random Forest |
| Deep Learning | TensorFlow / Keras MLP |
| Scalable pipeline | Spark MLlib |
| Language | Python 3.10+ |

---

## How to run

### Google Colab (recommended — no installation needed)
1. Go to [colab.research.google.com](https://colab.research.google.com)
2. Click **File → Upload notebook** and upload `cosmic_census_en.ipynb`
3. Run cell 0 (installs dependencies automatically)
4. Run all remaining cells with **Runtime → Run all**

### Locally (VSCode or Jupyter)
Prerequisites: Python 3.10+, Java 8 or 11 (required for Spark)

```bash
pip install -r requirements.txt
jupyter notebook cosmic_census_en.ipynb
```

---

## Pipeline

```
[SDSS CSV]  →  [Parquet Data Lake]  →  [PySpark: cleaning + features]
    →  [Pandas: EDA + Plotly]  →  [TensorFlow: classification]
    →  [Evaluation + Spark MLlib Pipeline]
```

---

## Topics covered

| Module | What is applied |
|---|---|
| Big Data principles | The 5 Vs, ecosystem, data lake |
| Hadoop & storage | HDFS vs RDBMS, Parquet as Data Lake |
| PySpark | SparkSession, RDDs, DataFrames, MapReduce |
| Pandas + Plotly | Full EDA, 5 interactive visualizations |
| Big Data Analytics | KDD pipeline, Random Forest, neural network |

---

## Dataset

- **Source:** [Sloan Digital Sky Survey DR17](https://skyserver.sdss.org)
- **Size:** 100,000 observations × 18 features
- **Classes:** GALAXY (59.4%), STAR (21.6%), QSO/Quasar (19%)
- **License:** Public domain (SDSS)

---

*Portfolio project — Big Data Topics in Python · Computer Engineering*
