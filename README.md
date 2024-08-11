# Navigating the Git Repository

Overview
This project analyzes movie data from 2010 - 2018 with the intent of identifying the most important varibales impacting a movie's success. 
***

Data Sources
1. IMDB - im.db
- Includes 8 different tables, we focus on movie_basics, movie_ratings, directors, and writers tables
2. bom.movie_gross.csv
- Contains key financial information including foreign and domestic gross income

Presentation Links
- insert PDF presentation here


Data Understanding
***
Dataset Overview
Summary: The datasets contain records on movie name, genre, year, length, director, writer, gross income, and other key variables. 

![movie_data_erd](https://github.com/user-attachments/assets/d2be31c9-7091-498d-baae-63dee4ed95af)


Important Data Columns:
1. Movie Basics
- Primary Title
- Start Year
- Runtime Minutes
- Genres

2. Movie Ratings
- Average Rating
- Num of Votes
  
![image](https://github.com/user-attachments/assets/6b9e299f-7de3-4674-954d-739140e76a54)

3. Writers / Director
- Primary Name
- Role 

---
Data Preparation
--- 
Combine movie_basics and movie_ratings tables to evaluate key variables.
![image](https://github.com/user-attachments/assets/b8cd7c59-523f-4dc8-ae43-1e678a23c493)

---
Exploratory Data Analysis
---
Group genres together to evaluate the best-performing genres across rating, number of votes, and gross income
![image](https://github.com/user-attachments/assets/10e79eb1-04d2-46f8-a940-9ccfe51a4f35)
The top 5 genres by average rating are:
Short
Documentary
Game-Show
News
Biography

Number of Votes By Genre
![image](https://github.com/user-attachments/assets/dbffc56a-b535-4c76-a554-a60dc25314d5)
