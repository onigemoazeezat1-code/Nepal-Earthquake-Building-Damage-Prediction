# Nepal Earthquake Building Damage Prediction

Predicting severe structural damage in buildings affected by the 2015 Nepal earthquake using high-performance SQL data engineering with DuckDB and tree-based machine learning models.

---

### Key Features

* **High-Performance Data Pipeline:** Leverages DuckDB for fast in-memory CSV joins and data transformation, outperforming SQLite speed.
* **Target Feature Engineering:** Consolidates multi-class damage grades into a binary classification task (`1` = Severe Damage Grade 4 or 5, `0` = Non-severe).
* **Machine Learning Pipelines:** Demonstrates complete end-to-end classification modeling using `scikit-learn` and `category_encoders`.

---

### Dataset Architecture

The project processes data across four primary tables from the Nepal earthquake dataset:

| Table | Description |
| :--- | :--- |
| `building_structure` | Architectural specs (floors, age, plinth area, height, foundation) |
| `building_damage` | Post-earthquake damage assessment and damage grade |
| `household_demographics` | Household and demographic details |
| `id_map` | Mapping key between households, buildings, and district IDs |

---

### Tech Stack

* **Language:** Python 3.10+
* **Data Engine & Storage:** DuckDB, SQLite, Pandas
* **Machine Learning:** scikit-learn, Category Encoders
* **Visualization:** Matplotlib

---

Results & Findings
Data Imbalance: Approximately 64.26% of buildings in the analyzed region (Gorkha district) suffered severe damage (Grade 4/5).

Query Performance: Query execution with DuckDB proved significantly faster than standard SQLite file queries for large aggregations.
