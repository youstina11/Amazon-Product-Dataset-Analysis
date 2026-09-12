![DiscountDecoded banner](./banner.svg)

# DiscountDecoded 🔍
### Amazon Product Dataset Analysis

A data analysis project exploring pricing, ratings, and review patterns across 1,400+ Amazon products — uncovering how discounts, categories, and customer sentiment actually relate to one another.

📄 **[View the full report on Gamma →](https://gamma.app/docs/Amazon-Product-Dataset-Analysis-dx347m99ktol2oi)**

---

## 📊 Overview

This project analyzes a real-world Amazon product dataset containing pricing, discount, rating, and review data to answer a simple question: **do bigger discounts mean happier customers?**

Spoiler: not really.

## 🗂️ Dataset

| Metric | Value |
|---|---|
| Total records | 1,465 |
| Unique products | 1,351 |
| Categories | 9 (Electronics, Computers & Accessories, Home & Kitchen, etc.) |
| Price range | ₹39 – ₹77,990 |
| Total reviews analyzed | 26.7M+ |

**Columns:** `product_id`, `product_name`, `category`, `discounted_price`, `actual_price`, `discount_percentage`, `rating`, `rating_count`, `about_product`, `user_id`, `user_name`, `review_id`, `review_title`, `review_content`, `img_link`, `product_link`

## 🔑 Key Findings

- **Average rating:** 4.1 / 5 across the dataset
- **Average discount:** 47.7% — nearly half of listed price, on average
- **Discount vs. rating correlation:** -0.16 — weak and slightly negative, meaning steep discounts don't reliably predict happier customers
- **Electronics dominates engagement**, accounting for 15.7M+ of the 26.7M total reviews
- Top-reviewed products (400K+ reviews each) are all budget accessories — HDMI cables, wired earphones — not high-ticket items

## 🧹 Data Cleaning Steps

Raw data required cleaning before analysis:
- Stripped `₹` currency symbols and comma-separated thousands from price fields
- Converted `discount_percentage` from string (`"64%"`) to numeric
- Parsed comma-formatted `rating_count` strings into integers
- Split pipe-delimited nested `category` strings (e.g. `Computers&Accessories|Accessories&Peripherals|...`) into a top-level category field
- Handled missing values in `rating` and `rating_count`

## 🛠️ Tools Used

- Python
- Pandas
- Gamma (for the presentation/report)

## 📁 Project Structure

```
├── amazon.csv          # Raw dataset
├── analysis.py          # Data cleaning & analysis script
└── README.md            # You are here
```

## 🚀 Getting Started

```bash
pip install pandas
python analysis.py
```

## 📬 Contact

Feel free to reach out or open an issue if you spot something interesting in the data I missed.

---
⭐ If you found this useful, consider starring the repo!
