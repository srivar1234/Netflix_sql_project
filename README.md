# 🎬 Netflix Movies & TV Shows — SQL Data Analysis Project

This project analyzes the **Netflix Titles Dataset** using pure **SQL**.
It covers **15 real-world business problems**, exploring insights such as most common ratings, genre distributions, country-wise releases, actor appearances, and much more.

![Netflix Logo](https://github.com/srivar1234/Netflix_sql_project/blob/main/logo.png)

---

## 📌 **Project Overview**

The goal of this project is to practice data cleaning and analytical querying using PostgreSQL.
The dataset contains details about Netflix Movies and TV Shows:

* Title
* Director
* Cast
* Country
* Rating
* Release year
* Date added to Netflix
* Genre
* Duration (minutes or seasons)

A table named **`netflix`** was created containing these fields, and all analysis was performed on it.

---

## 🗂 **Dataset Schema**

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

# 📊 **Business Problems & SQL Solutions**

Below are the **15 analytical SQL tasks** performed:

---

## 1️⃣ Movies vs TV Shows Count

Find how many Movies and TV Shows are on Netflix.

---

## 2️⃣ Most Common Rating by Category

Identify the most frequent rating for **Movies** and **TV Shows** separately.

---

## 3️⃣ Movies Released in Year 2020

Filter all movies released in a specific year.

---

## 4️⃣ Top 5 Countries with Most Content

Break down multi-value country fields and count contributions.

---

## 5️⃣ Longest Movie

Extract numeric minutes and sort to find the movie with the highest duration.

---

## 6️⃣ Content Added in the Last 5 Years

Convert text dates using `to_date()` and filter based on recent additions.

---

## 7️⃣ Content by Director “Rajiv Chilaka”

Find all Movies/TV Shows directed by this Indian filmmaker.

---

## 8️⃣ TV Shows with More Than 5 Seasons

Extract the numeric part from “X Seasons” and filter.

---

## 9️⃣ Count Content Items per Genre

Split genre fields into separate rows and group by genre.

---

## 🔟 Average Content Released per Year in India

Calculate yearly distribution and show the years with highest releases.

---

## 1️⃣1️⃣ Movies in the “Documentaries” Genre

Identify all documentary films on Netflix.

---

## 1️⃣2️⃣ Content Without a Director

List entries missing director information.

---

## 1️⃣3️⃣ Salman Khan Movies Added in Last 10 Years

Check actor presence in cast field and filter by date.

---

## 1️⃣4️⃣ Top 10 Actors in Indian Content

Unnest all actors and count appearances.

---

## 1️⃣5️⃣ Categorize Content (Good/Bad) Based on Keywords

If description contains **“kill”** or **“violence”**, label as **Bad**, otherwise **Good**.

---

# 🧠 **Conclusion**

This SQL analysis project demonstrates:

✔ Text processing (`split_part`, `string_to_array`, `unnest`)
✔ Date parsing using `to_date()`
✔ Window functions (`rank() over`)
✔ Aggregations & grouping
✔ Real-world data cleaning challenges
✔ Categorization & conditional logic

