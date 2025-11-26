# Web-Scrapping-Using-Python
---

# 📘 **README – Amazon Product Scraper (Playwright + Python)**

## 🚀 Overview

This project is a **Python-based Amazon product scraper** that uses **Playwright** (for browser automation) and **Selectolax** (for fast HTML parsing).
It extracts product **titles and prices** from Amazon search result pages and displays them in a clean tabular format.

This scraper is dynamic, fast, and capable of handling Amazon's JavaScript-rendered content.

---

## 🧰 Features

* Scrapes **Amazon search results** using real browser automation
* Extracts:

  * Product Title
  * Product Price
* Filters products based on **minimum & maximum price range**
* Sorts results **from lowest to highest price**
* Works across **multiple pages**
* Clean output using formatted tables
* Includes delay handling to reduce blocking
* Reliable scraping using dynamic page rendering

---

## 🛠️ Technologies Used

| Library        | Purpose                                      |
| -------------- | -------------------------------------------- |
| **Playwright** | Load Amazon pages dynamically using Chromium |
| **Selectolax** | Fast HTML tree parsing using CSS selectors   |
| **Tabulate**   | Display data in grid tables                  |
| **time**       | Add scraping delay                           |
| **re**         | Clean and extract numeric price values       |

---

## 📦 Installation

### 1️⃣ Install required libraries

```bash
pip install playwright selectolax tabulate
```

### 2️⃣ Install Playwright browsers

```bash
playwright install
```

---

## ▶️ Usage

### Run the script:

```bash
python scraper.py
```

### Input Required:

* Number of pages you want to scrape (Example: 3)

The script then:

1. Visits each Amazon search page
2. Extracts product data
3. Filters by price
4. Sorts them
5. Prints clean tables

---

## 📝 Code Summary

The program:

1. Loads Amazon pages using Playwright
2. Extracts HTML content
3. Uses Selectolax to parse:

   * Product title
   * Product price
4. Cleans the price using regex
5. Filters products within:

   ```
   MIN_PRICE = 9000
   MAX_PRICE = 150000
   ```
6. Displays results using **tabulate**
7. Moves to next pages until scraping is complete

---

## 📊 Example Output

```
+-----------------------------------------------------+----------+
| Title                                               | Price    |
+-----------------------------------------------------+----------+
| Samsung Galaxy M34 5G                               | 12999.0  |
| Redmi Note 13 Pro                                   | 15999.0  |
| iQOO Z7 Pro 5G                                      | 21999.0  |
+-----------------------------------------------------+----------+
```

---

## ⚠️ Disclaimer

This scraper is for **educational purposes only**.
Amazon does not permit scraping their website.
Use responsibly and only for learning/testing with caution.


