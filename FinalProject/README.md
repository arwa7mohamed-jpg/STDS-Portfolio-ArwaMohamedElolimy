# ⚡ Final Project: GreenStream Energy Data Pipeline Design

## 📖 Project Overview
This project involves designing a comprehensive **Serverless ETL Pipeline** for **GreenStream Energy**. The goal is to architect a solution that ingests, cleans, and stores high-frequency data from thousands of IoT Smart Meters in a cloud environment.

The solution moves away from manual processing to an automated **Event-Driven Architecture**, ensuring data quality and availability for analytics.

---

## 🏗 Architecture Components (Task A)
The pipeline is designed using a **Cloud-Native approach** covering the following stages:
1.  **Source:** IoT Smart Meters transmitting raw CSV data.
2.  **Ingestion:** Raw storage in a Data Lake (S3 Bucket).
3.  **Processing:** An Event-Triggered ETL Function (Serverless) for validation and transformation.
4.  **Storage:**
    - **Data Warehouse:** For clean, structured data (SQL).
    - **Data Archive:** For historical data in **Parquet** format.
    - **Error Handling:** A dedicated path for logging invalid records.

> *Note: The full architecture diagram is included in the project documentation PDF.*

---

## ⚙️ Transformation Rules (Task B)
The ETL process applies specific business logic to ensure data integrity:

| Rule Name | Logic Applied |
| :--- | :--- |
| **Unit Standardization** | Converts "W" (Watts) to "kW" by dividing by 1000. |
| **Missing Values** | Flags records with NULLs as "Incomplete" (without deleting them). |
| **Faulty Meter Detection** | Identifies meters reporting `0` consumption for >24 hours. |
| **Format Optimization** | Converts CSV inputs to columnar **Parquet** format for the archive. |

---

## 🔄 Data Lifecycle (Task C)
The project documents the complete journey of a single record:
1.  **Ingestion:** Meter sends `1500 W` CSV file.
2.  **Trigger:** Cloud storage event triggers the ETL code.
3.  **Transform:** Value converted to `1.5 kW`.
4.  **Load:** Clean data saved to Database; Copy archived as Parquet.
5.  **Monitor:** Errors (if any) are routed to logs for review.

---

## 📂 Included Files
- **`Final Project.pdf`**: The complete design document containing the Architecture Diagram, Business Rules, and Lifecycle scenario.

---

### 🛠 Tools & Concepts Used
- **Diagramming:** Draw.io
- **Concepts:** ETL, Data Engineering, Event-Driven Architecture, Data Warehousing.