# 🏢 AmbitionBox Companies Web Scraper

This project scrapes company information from [AmbitionBox](https://www.ambitionbox.com/list-of-companies) — a platform for company reviews, salaries, and job listings.  
The script automatically collects company details from all pages (1–502) and stores them in a single CSV file for further analysis.

---

## 📌 Features

- 🔍 Scrapes data from 500+ AmbitionBox pages  
- 📊 Extracts:
  - Company Name  
  - Rating  
  - Number of Reviews  
  - Salary Count  
  - Job Openings  
  - Company Description / Industry Info  
- ⚡ Handles missing data gracefully  
- 🧾 Saves all results to `ambitionbox_companies.csv`

---

## ⚙️ Requirements

Make sure you have the following Python libraries installed:

```bash
pip install requests beautifulsoup4 lxml pandas
```

---

## 🚀 How to Run

1. **Clone or copy** the Python script.
2. Run the file in your terminal or any IDE:
   ```bash
   python ambitionbox_scraper.py
   ```
3. Wait for the script to finish scraping all pages.
4. Once done, you’ll see:
   ```
   ✅ Scraping completed!
   ```
5. The results will be saved as:
   ```
   ambitionbox_companies.csv
   ```

---

## 🧠 How It Works

1. Loops through **pages 1 to 502** of AmbitionBox.  
2. Sends HTTP requests using custom headers (to avoid blocking).  
3. Parses each webpage with **BeautifulSoup (lxml)**.  
4. Extracts:
   - Company name (`<h2>`)
   - Rating (`div` with style)
   - Review count (`span` class)
   - Salary & job counts (links containing `/salaries/` or `/jobs/`)
   - Description text  
5. Appends all data into a single Pandas DataFrame.  
6. Exports the final result to CSV.

---

## 🧩 Example Output (First Few Rows)

| Name              | Rating | Reviews | Salary | Jobs | Description           |
|-------------------|--------|----------|---------|------|------------------------|
| TCS               | 4.1    | 25k      | 10k     | 2k   | IT Services & Consulting |
| Infosys           | 4.0    | 21k      | 9k      | 1.5k | IT Services & Consulting |
| Accenture         | 4.2    | 30k      | 8k      | 1k   | IT Services & Consulting |

---

## 🧾 Output File

After execution, you’ll get:
```
ambitionbox_companies.csv
```

This file contains all company data across pages 1–502.

---

## ⚠️ Note

- This scraper is for **educational and research purposes only**.  
- Frequent scraping may violate website **terms of service**.  
- Use responsibly and respect site bandwidth.

---

## 🧑‍💻 Author

**Yashwant Kumar Chitchula**  
B.Tech CSE (AI & ML) @ VIT Chennai  


---
