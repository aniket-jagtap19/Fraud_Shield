# Fraud_Shield

## Overview (working!)
Fraud_Shield is a real-time fraud detection pipeline using Kafka, Spark Streaming, and an Isolation Forest ML model to detect anomalous transactions and store results in MinIO.

## Architecture
- **Kafka Producer**: Generates synthetic transactions  
- **Spark Streaming Consumer**: Processes data & detects fraud  
- **ML Model**: Isolation Forest for anomaly detection  
- **MinIO**: Stores flagged transactions  
- **PostgreSQL**: Optional future storage  

## Project Structure
```
├── scripts
│   ├── kafka_transaction_producer.py  # Generates and sends transactions to Kafka
│   ├── spark_streaming_consumer.py    # Consumes transactions from Kafka, applies fraud detection
│   ├── train_isolation_forest.py      # Trains and saves the Isolation Forest model
│   ├── isolation_forest_model.pkl     # Trained machine learning model
│
├── docker-compose.yml                 # Orchestrates services (Kafka, Spark, MinIO, PostgreSQL)
├── requirements.txt                    # Python dependencies
├── minio-entrypoint.sh                 # Initialization script for MinIO
└── README.md                           # Project documentation
```

## Technologies Used
- **Apache Kafka**: Message broker for real-time transaction streaming.
- **Apache Spark (Structured Streaming)**: Consumes transaction data and applies fraud detection.
- **Scikit-learn (Isolation Forest)**: Machine learning model for anomaly detection.
- **MinIO (S3-Compatible Storage)**: Stores fraudulent transactions.
- **PostgreSQL**: Future storage for transaction logs.

## Future Improvements
- Store transaction logs in PostgreSQL.
- Enhance the fraud detection model with additional features.
- Implement alerting for fraudulent transactions.
<!-- Project by Aniket Jagtap,  time: - 2026-08-28 22:48:22 -->

<!-- Project by Aniket Jagtap,  time: - 2026-08-28 22:58:41 -->

<!-- Project by Aniket Jagtap,  time: - 2026-08-28 23:13:58 -->

<!-- Project by Aniket Jagtap,  time: - 2026-08-31 09:40:14 -->

<!-- Project by Aniket Jagtap,  time: - 2026-08-31 17:57:14 -->

<!-- Project by Aniket Jagtap,  time: - 2026-09-03 22:21:58 -->
