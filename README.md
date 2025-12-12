# 📊 Zepto SQL Data Analysis Project

This project focuses on analyzing inventory and product data from Zepto, one of India’s leading quick-commerce platforms.
The objective of the project is to understand product attributes, stock availability, pricing, discounts, and category patterns using SQL.

---

## 🗂️ Dataset Description

The dataset contains product-level inventory information.
Key fields include:

| Column                     | Description                                       |
| -------------------------- | ------------------------------------------------- |
| **category**               | Product category (e.g., Dairy, Snacks, Beverages) |
| **name**                   | Product name                                      |
| **mrp**                    | Maximum Retail Price                              |
| **discountPercent**        | Discount applied on the product                   |
| **discountedSellingPrice** | Final selling price after discount                |
| **availableQuantity**      | Number of units available                         |
| **weightInGms**            | Weight of the product                             |
| **outOfStock**             | Indicates if the item is currently unavailable    |
| **quantity**               | Units per package                                 |

---

## 🛢️ Database Structure

The table used for analysis:

```sql
CREATE TABLE zepto (
  unit_id SERIAL PRIMARY KEY,
  category VARCHAR(120),
  name VARCHAR(150) NOT NULL,
  mrp NUMERIC(8,2),
  discountPercent NUMERIC(5,2),
  availableQuantity INTEGER,
  discountedSellingPrice NUMERIC(8,2),
  weightInGms INTEGER,
  outOfStock BOOLEAN,
  quantity INTEGER
);
```

This structure ensures proper data types for financial values, product attributes, and inventory flags.

---

## 🔎 Analysis Overview

The SQL analysis focuses on understanding:

* Product pricing and discount patterns
* Stock availability and out-of-stock trends
* Category-wise product distribution
* High-value and low-value items
* Variations between MRP and final selling price
* Weight and quantity insights

Each query is designed to answer a specific business-oriented question.

