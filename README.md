# 🎯 Sales Ops · Myanmar Lead Classifier

A high-performance, advanced **Streamlit** application built for Delivery Hero / foodpanda Myanmar. This tool cleans, classifies, and deduplicates Food & Beverage (F&B) sales leads scraped from Google Maps (via Apify) against your master CRM database (Salesforce).

---

## 🚀 Key Features

* **Nationwide Myanmar Scope (`MM`):** Automatically filters Apify scraping results for Myanmar. Includes Burmese Unicode text normalization and town/township spatial matching.
* **Smart Phone Number Standardization:** Automatically strips special characters, handles the `+95` country code, and formats numbers to standard local `09` formats.
* **Tri-Lingual Category Matching:** Pre-configured with F&B keywords in **English**, **Burmese** (e.g., စားသောက်ဆိုင်, ကော်ဖီဆိုင်), and **Chinese** (e.g., 烧烤, 火锅) to identify delivery-eligible businesses.
* **High-Speed O(1) Hash Matching:** Instantly deduplicates incoming leads against large master datasets using pre-indexed hash sets for GRID IDs and standardized phone numbers.
* **Fuzzy & Geospatial Matching:** Utilizes `rapidfuzz` for high-accuracy text similarity and `geopy`/Haversine formulas to match nearby leads within a customizable GPS radius.
* **Apify Workflow Automation:** Automatically generates Google Maps search URLs from your raw leads and seamlessly merges the returned Apify data back with your original internal `GRID` IDs.
* **Rich Excel Export:** Downloads classified results directly as a multi-sheet, color-coded `.xlsx` file using `openpyxl`.

---

## 🛠️ Installation & Setup

### 1. Prerequisites
Ensure you have Python 3.8+ installed. The app requires several libraries for data processing and string matching.

### 2. Set up a Virtual Environment (Recommended)
```bash
python -m venv venv

# Activate on macOS/Linux:
source venv/bin/activate  

# Activate on Windows:
venv\Scripts\activate
