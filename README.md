# 🌤️ ETL Weather Pipeline with Apache Airflow & Docker

This project demonstrates a production-ready ETL pipeline that fetches, processes, and stores weather data using **Apache Airflow**, **Docker**, and **Python**.

> Built to showcase data engineering practices like DAG orchestration, task modularity, environment-based config management, and pipeline testing.

---

## 🚀 Features

- ⏱️ **Scheduled DAG** to fetch weather data from OpenWeatherMap or similar APIs.
- 🛠️ **ETL logic** with Python: extract → transform → load.
- 🐳 **Dockerized setup** for local development with Airflow Web UI.
- ✅ **Modular tasks** using Airflow’s TaskFlow API and custom operators.
- 🧪 **Pytest-based DAG testing** included.
- 📦 Easily extensible to add new APIs or data sinks (S3, DB, etc.).

---

## 🧱 Tech Stack

| Tool              | Purpose                       |
|-------------------|-------------------------------|
| Apache Airflow    | DAG orchestration             |
| Docker Compose    | Container orchestration       |
| Python 3.10+      | ETL logic and API calls       |
| pytest            | DAG testing                   |

---

## 📂 Project Structure

```bash
etl_weather/
├── dags/                   # DAG definitions
│   └── etl_weather.py
├── include/                # External files (optional)
├── plugins/                # Custom operators/hooks (if any)
├── tests/                  # Pytest-based DAG unit tests
│   └── dags/
│       └── test_etl_weather.py
├── Dockerfile              # Airflow image customization
├── docker-compose.yml      # Multi-container orchestration
├── airflow_settings.yaml   # Preconfigured connections/variables
├── requirements.txt        # Python dependencies
├── packages.txt            # OS-level dependencies (apt)
├── README.md               # Project overview & usage
└── .gitignore              # Ignored files and folders