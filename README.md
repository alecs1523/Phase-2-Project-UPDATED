# Navigating the Git Repository

Overview
This project analyzes movie data from 2010 - 2018 with the intent of identifying the most important varibales impacting a movie's success. 
***
![download](https://github.com/user-attachments/assets/3fc35d5c-d57d-44c7-b3e1-3f75ea0bdc9f)

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
- Short
- Documentary
- Game-Show
- News
- Biography

Number of Votes By Genre
![image](https://github.com/user-attachments/assets/dbffc56a-b535-4c76-a554-a60dc25314d5)
---
The combined rating for genres by calculating the rank of votes and rating (the lower the score the higher the rank)
![image](https://github.com/user-attachments/assets/2dac4a9d-ee35-4d16-8c15-c0d38bb665fc)

Observations from Graph:

This graph shows rankings with the lowest bar indicating the highest combined rating between votes and rank
Biography, Adventure, Animation, Sport, Music are the top 5

---
Top writers based on average number of votes (must have written 20 or more films)
![image](https://github.com/user-attachments/assets/9ddc111f-f673-4963-919b-419893300065)

--- 
Top Directors
![image](https://github.com/user-attachments/assets/98c6a80b-0883-421e-8109-31f5e56caa32)

--- 
Movie Length 
---
![image](https://github.com/user-attachments/assets/5f7cee9a-998d-43cd-b08a-daa9532967cc)

Observations from this graph:

Movies with lengths in the 0-75 and 240+ minutes buckets tend to have higher median ratings compared to other buckets.
Movies in the 76-240 minutes range have relatively consistent median ratings, but with more lower-end outliers.
***
---
Gross Income Dataset (bom.movie_gross.csv.gz)
---
The dataset only contains data dating back to 2010 which is recent enough to include all the data

We will filter on the top 2,000 grossing movies out of the 6,915 in the dataset to focus on the most successful films
![image](https://github.com/user-attachments/assets/d5c3eb5d-b6e0-4540-9209-b08e09af7457)

---
Top Genres By Gross Income Per Year
---
![image](https://github.com/user-attachments/assets/a601527e-b371-493a-98b4-eee0ea26830f)
Takeaways from above graph:
- Adventures seems to have the highest gross income every year
- Action is #2

---
YoY % Change in Gross Income By Genre
---
![image](https://github.com/user-attachments/assets/085b9553-c18b-4934-8fef-f8492c1c224e)

--- 
Percentage Change In Gross Income from 2010-2018
---
1. Action increased 75%
2. Adventure increased 47%
3. Comedy increased 8%
   
---
Conclusions
---
- Focus on the top grossing genres: Action, Adventure, & Sci-Fi
- Movie lengths should be around 120 minutes
- Strictly use writers and directors in the top 2/3 of average rating, the dropoff in the bottom third is substantial

---
Recommendations
---
Recomendations
My recommendation is to focus on a narrow subset of films with genres being Action, Adventure, and/or Sci-Fi, movie length should be around 120 minutes, and directors / writers should have 20 movies under their belt and in top 2/3 of average rating.
This recommnedation is supported by 4 key pieces of evidence:
- Action, Adventure, and Sci-Fi films have the highest gross income, average rating, and number of votes
- Movie lengths in the 120 minute bucket received the highest number of votes
- The difference between writers / directors in the top 2/3 versus the bottom 1/3 is substantial
