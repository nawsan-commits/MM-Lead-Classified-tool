# 🍔 Lead Classifier — Myanmar Nationwide

A high-performance **Streamlit** application designed to clean, classify, and deduplicate F&B (Food & Beverage) sales leads scraped from Google Maps or Apify against a master database (Salesforce / Backend Accounts).

---

## 🚀 Key Features

- **Nationwide Myanmar Scope (`MM`):** Automatically filters leads exclusively for Myanmar using latitude and longitude geographic boundaries.
- **Multi-Language Category Matching:** Pre-configured with F&B keywords in **English**, **Burmese** (e.g., စားသောက်ဆိုင်, ကော်ဖီဆိုင်), and **Chinese** (e.g., 烧烤, 珍珠奶茶店, 火锅).
- **Auto Phone Number Standardization:** Automatically strips special characters, handles the `+95` Myanmar country code, and formats numbers to standard local 9-to-11 digit formats (e.g., `09...`).
- **High-Speed Hash Matching ($O(1)$ Complexity):** Instantly deduplicates incoming leads against large master datasets using pre-indexed hash sets for standardized phone numbers.
- **Instant Export:** Download the net-new, classified results directly as a clean CSV file.

---

## 🛠️ Prerequisites

Make sure you have Python 3.8 or higher installed on your machine. You will also need `pip` to install the required libraries.

---

## ⚙️ Installation & Setup

1. **Clone or Download the Repository:**
   Place the `app.py` file into a new project folder.

2. **Set up a Virtual Environment (Recommended):**
   ```bash
   python -m venv venv
   
   # Activate on macOS/Linux:
   source venv/bin/activate  
   
   # Activate on Windows:
   venv\Scripts\activate
