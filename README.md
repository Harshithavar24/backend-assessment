## 📄 Backend Assessment – Data Pipeline

### 🎯 Objective

Built a Dockerized data pipeline integrating:

* Flask (Mock API)
* FastAPI (Data Ingestion Service)
* PostgreSQL (Database)

---

### 🏗 Architecture

Flask API → FastAPI Pipeline → PostgreSQL

---

### ⚙️ Services

#### 1. Mock Server (Flask)

* Provides customer data from JSON
* Supports pagination
* Endpoints:

  * `/api/customers`
  * `/api/customers/{id}`
  * `/api/health`

---

#### 2. Pipeline Service (FastAPI)

* Fetches data from Flask API
* Stores data in PostgreSQL
* Implements upsert logic
* Endpoints:

  * `/api/ingest`
  * `/api/customers`
  * `/api/customers/{id}`

---

#### 3. Database (PostgreSQL)

* Stores customer data
* Primary Key: `customer_id`

---

### 🐳 Run Project

```bash
docker compose up --build
```

---

### 📌 Note

Due to local virtualization issues, this project was executed using GitHub Codespaces.

---

### ✅ Features

* Pagination
* Upsert logic
* REST APIs
* Dockerized architecture

---

### 📦 Tech Stack

* Flask
* FastAPI
* PostgreSQL
* Docker
* SQLAlchemy
