# Salesforce Data Cloud Demo

## Overview

This repository contains sample datasets used for demonstrating an end-to-end Salesforce Data Cloud implementation.

The datasets simulate a retail/e-commerce business where customer information, orders, website interactions, and product information are collected from different systems and unified inside Salesforce Data Cloud to build a Customer 360 view.

These files can be used to demonstrate:

- Data Stream ingestion
- Data Mapping (DLO → DMO)
- Identity Resolution
- Unified Individual Profiles
- Calculated Insights
- Segmentation
- Data Cloud Analytics
- Personalization use cases

---

## Repository Structure

| File | Description |
|------|-------------|
| **Demo_Customers.csv** | Master customer profile data containing customer demographic information such as Customer ID, Name, Email, Phone, Gender, City, Country, etc. This acts as the primary customer dataset. |
| **Demo_Orders.csv** | Transactional order history containing Order IDs, Customer IDs, Products Purchased, Order Date, Quantity, Price, Order Status, and Total Amount. Used to build customer purchasing behaviour and revenue insights. |
| **Demo_Website_Activity.csv** | Website interaction events including page visits, product views, searches, cart additions, and other digital engagement activities. Used for behavioural analytics and audience segmentation. |
| **Demo_Product_Catalogue.csv** | Product master dataset containing Product IDs, Product Names, Categories, Brands, Pricing, and Product Attributes. Used to enrich transactional data. |
| **Data_Cloud_Demo_CSVs.zip** | ZIP archive containing all demo CSV files for easy download and import into Salesforce Data Cloud. |

---

# Dataset Relationships

The datasets are connected using common identifiers.

```
Customers
    │
    ├───────────────┐
    │               │
Orders         Website Activity
    │
    │
Product Catalogue
```

### Primary Keys

| Dataset | Primary Key |
|----------|-------------|
| Customers | CustomerID |
| Orders | OrderID |
| Products | ProductID |
| Website Activity | ActivityID |

### Foreign Keys

| Source | References |
|---------|------------|
| Orders.CustomerID | Customers.CustomerID |
| Orders.ProductID | ProductCatalogue.ProductID |
| WebsiteActivity.CustomerID | Customers.CustomerID |

---

# Typical Salesforce Data Cloud Flow

```
CSV Files

      ↓

Data Streams

      ↓

Data Lake Objects (DLO)

      ↓

Data Model Objects (DMO)

      ↓

Identity Resolution

      ↓

Unified Individual

      ↓

Calculated Insights

      ↓

Segments

      ↓

Analytics / Activation
```

---

# Example Use Cases

These datasets can be used to demonstrate:

- Customer 360
- Customer Lifetime Value
- Purchase Frequency
- High Value Customers
- Inactive Customers
- Website Engagement
- Product Performance
- Cross-sell Opportunities
- Personalized Marketing
- Customer Segmentation
- Executive Dashboards

---

# Sample Business Scenario

A retail company stores customer information in its CRM, receives orders from an e-commerce platform, tracks website behaviour through digital analytics, and maintains products in a catalog system.

Salesforce Data Cloud ingests data from all these systems, unifies customer identities, and creates a single Customer 360 profile that can be used for analytics, segmentation, and AI-driven personalization.

---

# Prerequisites

Before importing these files into Salesforce Data Cloud:

- Enable Salesforce Data Cloud
- Create Data Streams
- Configure Data Lake Objects (DLOs)
- Map to Data Model Objects (DMOs)
- Configure Identity Resolution Rules
- Create Calculated Insights
- Build Segments
- Create Dashboards or activate audiences

---

# Notes

- All datasets are intended for demonstration and learning purposes.
- Customer information is fictional.
- Data formats are designed to align with common Salesforce Data Cloud ingestion patterns.
- The datasets can be extended with additional records to simulate enterprise-scale implementations.

---

# Author

Created as part of a Salesforce Data Cloud learning and demonstration project showcasing end-to-end Customer 360 implementation using Salesforce Data Cloud.
