# 🎬 Netflix Movies & TV Shows — SQL Data Analysis Project

![Netflix Logo](https://github.com/srivar1234/Netflix_sql_project/blob/main/logo.png)

---

## 🏷️ Badges

![SQL](https://img.shields.io/badge/SQL-Analysis-blue?style=for-the-badge)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-blue?style=for-the-badge)
![GitHub](https://img.shields.io/badge/GitHub-Project-black?style=for-the-badge)
![Data Analysis](https://img.shields.io/badge/Data_Analysis-Project-brightgreen?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

---

# 📚 Table of Contents
1. [Project Overview](#project-overview)  
2. [Dataset Schema](#dataset-schema)  
3. [Technologies Used](#technologies-used)  
4. [Screenshots](#screenshots)  
5. [Business Problems & SQL Solutions](#business-problems--sql-solutions)  
6. [Insights Summary](#insights-summary)  
7. [How to Run This Project](#how-to-run-this-project)  
8. [Author](#author)

---

# 📘 Project Overview

This project analyzes the **Netflix Titles Dataset** using **pure SQL on PostgreSQL**.  
It includes **15 real-world business problems**, focusing on:

- Content classification  
- Ratings distribution  
- Genre expansion  
- Country-level analysis  
- Actor appearances  
- Season analysis  
- Time-based filtering  

The project demonstrates **text processing, date parsing, window functions, CTE usage, unnesting arrays**, and more — all essential skills for a **Data Analyst / Data Engineer**.

---

# 🗂 Dataset Schema
Dataset Source: This dataset was downloaded from Kaggle: “Netflix Movies and TV Shows Dataset”.

```sql
create table netflix(
    show_id varchar(6),
    type varchar(10),
    title varchar(150),
    director varchar(208),
    casts varchar(1000),
    country varchar(150),
    date_added varchar(50),
    release_year int,
    rating varchar(10),
    duration varchar(15),
    listed_in varchar(100),
    description varchar(250)
);
```

---


# 📊 Business Problems & SQL Solutions

Below are the **15 SQL business use cases** solved in this project:

---

## **1️⃣ Movies vs TV Shows Count**
Count total number of Movies and TV Shows separately.

---

## **2️⃣ Most Common Rating by Category**
Find the highest occurring rating for Movies and TV Shows using window functions.

---

## **3️⃣ Movies Released in 2020**
Filter all movies released in a specific year.

---

## **4️⃣ Top 5 Countries with Most Netflix Content**
Explode comma-separated countries and count contributions.

---

## **5️⃣ Longest Movie**
Extract numeric minutes from duration and sort.

---

## **6️⃣ Content Added in Last 5 Years**
Convert string dates using `to_date()` and filter recent content.

---

## **7️⃣ Movies/TV Shows by Rajiv Chilaka**
Search for a specific director.

---

## **8️⃣ TV Shows with More than 5 Seasons**
Extract number from "X Seasons" using `split_part()`.

---

## **9️⃣ Number of Items per Genre**
Expand multi-value genres using `unnest()`.

---

## **🔟 Average Yearly Content Released (India)**
Analyze release trends country-wise.

---

## **1️⃣1️⃣ Documentary Movies**
Identify movies that fall in the “Documentaries” category.

---

## **1️⃣2️⃣ Content Without Director**
Find incomplete metadata.

---

## **1️⃣3️⃣ Salman Khan Movies in Last 10 Years**
Filter cast column and date column together.

---

## **1️⃣4️⃣ Top 10 Actors in Indian Content**
Expand casts array and count appearances.

---

## **1️⃣5️⃣ Content Categorization (Good vs Bad)**
Label descriptions containing "kill" or "violence" as **Bad**, others as **Good**.

---

# 📌 Insights Summary

Some meaningful insights derived from this project:

- Netflix has **more Movies** than TV Shows.
- **TV-MA** is the most common rating.
- The **US and India** contribute the highest number of titles.
- Many entries contain **multiple genres**.
- **Documentaries** form a significant content category.
- Actor appearances vary heavily depending on country.
- Most TV shows have **1–3 seasons**.
- Salman Khan appears in **very few Netflix items**.
- Content flagged as “Bad” (keywords kill/violence) is much lower than “Good”.

---

# 🛠 Technologies Used

- **PostgreSQL**
- **SQL**
- **GitHub**
- **CSV Data Processing**
- **Window Functions**
- **Text Manipulation**

---

# 🚀 How to Run This Project

### **1. Clone the Repository**
```bash
git clone https://github.com/srivar1234/Netflix_sql_project.git
```

### **2. Open PostgreSQL or pgAdmin**

### **3. Create the table using `solution.sql`**
```sql
\i solution.sql
```

### **4. Load the dataset**
Use pgAdmin → Import → `netflix_titles.csv`

### **5. Run individual SQL queries**
Each query corresponds to a specific business question.

---

# 👤 Author

**Srivar Karamsetty**  
Passionate about **Data Engineering**, **Cloud**, and **Advanced SQL**.  
This project is part of my journey to master real-world data analysis.

---

If you like this project, ⭐ star the repo!

