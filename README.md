# Brazillian-E-Commerce-Analysis
End-to-End E-Commerce Analytics & Churn Prediction using Databricks Lakehouse

📖 Project Overview

This project demonstrates an end-to-end, production-style data analytics solution built on the Databricks Lakehouse Platform.
It addresses real-world e-commerce business problems such as customer churn, revenue concentration, customer segmentation, and growth analysis using a Medallion Architecture (Bronze–Silver–Gold).

The solution includes data engineering, analytics, governance, orchestration, and machine learning, making it fully portfolio-ready.

🎯 Business Problem

An e-commerce company is facing:

Declining repeat purchases

High customer churn risk

Revenue concentration among limited products and regions

Objectives

Identify customers likely to churn

Segment customers for targeted marketing

Analyze product and regional revenue contribution

Provide executive-ready dashboards

Build a churn prediction ML model

📊 Dataset

Public e-commerce transactional dataset consisting of 9 relational tables, including:

Customers

Orders

Order Items

Payments

Products

Sellers

Reviews

Categories

Geolocation

Raw data is stored securely using Unity Catalog Volumes.

🏛️ Architecture & Data Flow
Medallion Architecture

Bronze: Raw ingestion from CSV files into Delta tables

Silver: Cleaned, standardized, and enriched business tables

Gold: Aggregated, business-ready datasets for analytics and ML

Governance

Unity Catalog for access control

Secure Volumes (Public DBFS disabled)

Role-based permissions

⚙️ Technologies Used

Databricks Lakehouse

Apache Spark (PySpark & SQL)

Delta Lake

Unity Catalog

Databricks SQL Dashboards

Databricks Workflows (Jobs)

MLflow (Model Tracking)

🥉 Bronze Layer

Raw CSV ingestion into Delta tables

No transformations

Metadata added (ingestion_timestamp, source_file)

Stored in Unity Catalog schemas

🥈 Silver Layer

Data cleaning and standardization

Duplicate removal

Timestamp normalization

Business-level joins (orders + customers + payments)

Designed for reusability across analytics and ML

🥇 Gold Layer

Gold tables directly solve business questions:

Gold Table	Business Purpose
customer_churn_features	Identify churn-risk customers
customer_segments	Marketing segmentation
product_revenue_performance	Revenue concentration
region_revenue_performance	Geographic insights
monthly_revenue_kpis	Growth & AOV tracking
📈 Analytics & Dashboard

An executive-level Databricks SQL Dashboard provides:

Revenue trends

Customer segmentation

Churn risk indicators

Top products

Regional performance

Dashboards are built directly on Gold tables to ensure metric consistency.

🤖 Machine Learning

Use Case: Customer churn prediction

Features engineered from Gold layer

Model trained using Logistic Regression / Random Forest

Experiments tracked using MLflow

Metrics logged for reproducibility

Key Insights

A small percentage of customers contribute the majority of revenue

Customers inactive for 90+ days show significantly higher churn risk

Repeat customers have higher average order value

Revenue is concentrated in specific products and regions

✅ Business Recommendations

Launch retention campaigns for high-risk customers

Prioritize high-value customer segments

Focus marketing spend on top-performing regions

Promote high-revenue products and review underperformers

👤 Author

Abhishek Panwar
Data Analyst / Analytics Engineer
Databricks | SQL | PySpark
