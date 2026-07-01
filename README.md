# restaurant-sales-analysis
This is my project where I explore a fast food restaurant's sales data. The data is from 2022 and 2023 (April 2022 to March 2023).  I want to clean the data first, then answer some basic questions about the sales, and finally make some charts to see everything visually.


## 📊 About the Dataset

The data covers sales from **April 2022 to March 2023** and contains **1000 orders**
with the following columns:

| Column | Description |
|---|---|
| `order_id` | Unique ID for each order |
| `date` | Date of the transaction |
| `item_name` | Name of the food/drink item ordered |
| `item_type` | Category of the item (Fastfood or Beverages) |
| `item_price` | Price of the item (in Rs) |
| `quantity` | Quantity ordered |
| `transaction_amount` | Total amount paid |
| `transaction_type` | How the customer paid (Cash, Online, Card Payment) |
| `received_by` | Who received the order (Male/Female) |
| `time_of_sale` | Time of day the order was placed (Morning, Afternoon, Evening, Night, Midnight) |

## 📁 Files in this Project

| File | Description |
|---|---|
| `Restaurant_Sales_Analysis.ipynb` | ---> main notebook with all the cleaning, analysis, and charts |
| `Balaji_Fast_Food_Sales.csv` | ---> The original raw dataset |
| `Cleaned_Balaji_Fast_Food_Sales.csv` | ---> dataset after cleaning  |
| `Cleaned_Balaji_Fast_Food_Sales.xlsx` | Same cleaned data, saved as an Excel file |
| `README.md` | This file |

## 🛠️ Tools & Libraries Used

- **Python 3**
- `pandas` – for loading, cleaning, and analyzing the data
- `numpy` – for some numerical operations
- `matplotlib` & `seaborn` – for making charts
- `psycopg2` & `sqlalchemy` *(optional)* – for loading the cleaned data into a local PostgreSQL database

## 🧹 Data Cleaning Steps

1. Checked and filled missing values in the `transaction_type` column (filled with `Card Payment`)
2. Standardized the date format and split `date` into separate `Day`, `Month`, and `Year` columns
3. Converted `Day`, `Month`, and `Year` to integer type
4. Simplified the `received_by` column by replacing `Mr.` / `Mrs.` with `Male` / `Female`
5. Saved the cleaned data as both `.csv` and `.xlsx` for future use

## ❓ Questions Answered

1. Which item is the most purchased and which is the least purchased?
2. What is the most common transaction type used by customers?
3. Which gender orders the most?
4. What is the most common time of sale?
5. Which item is the most expensive? Which is the least expensive?
6. Which year had more average sales — 2022 or 2023?
7. What is the average amount spent by male and female customers?

## 📈 Visualizations

The notebook includes the following charts to visually answer the questions above:

- Bar chart of product prices
- Pie chart of item type distribution (Fastfood vs Beverages)
- Horizontal bar chart of most/least ordered items (by quantity)
- Horizontal bar chart of total revenue by product
- Pie chart of transaction types
- Pie chart of time of sale
- Pie chart of customer gender distribution
- Bar chart comparing average sales by year (2022 vs 2023)
- Bar chart comparing average spend by gender

## 🔑 Key Findings

- **Cold Coffee** is the most purchased item; **Sandwich** is the least purchased
- **Cash** is the most used payment method
- **Male** customers place slightly more orders overall
- Most sales happen at **Night**, least happen in the **Morning**
- **Sandwich** is the most expensive item (Rs 60); **Aalopuri, Vadapav, and Panipuri** are the cheapest (Rs 20)
- **2022** had slightly higher average sales than 2023
- **Female** customers spend slightly more on average per transaction (~Rs 280) than male customers (~Rs 270), even though male customers order more often

## 🗄️ Bonus: Loading Data into PostgreSQL

At the end of the notebook, I added an optional step that connects to a local PostgreSQL
database (using `psycopg2` and `sqlalchemy`) and loads the cleaned CSV into a database table.
This part is optional and only works if you have PostgreSQL installed and running locally —
update the `host`, `database`, `user`, and `password` values in the connection function with
your own database credentials before running it (avoid hardcoding real passwords if sharing
this notebook publicly).


## 📝 Notes

This is a project made while learning Data Analysis and EDA with pandas and matplotlib. Feedback and suggestions are always welcome!

## 👤 Author
Bikash Sahani
github.com/bikashsahani | linkedin.com/in/bikash-sahani
