# MovieLens 100k Data Analysis

This project leverages Apache Zeppelin and Spark SQL to perform data analysis on the MovieLens 100k dataset. The analysis aims to explore user ratings, movie genres, and user demographics to extract meaningful insights.

> Dataset can be obtained from [MovieLens 100k Dataset](https://grouplens.org/datasets/movielens/100k/)

![Hollywood](images/hollywood.jpg)

## Project Overview

The MovieLens 100k dataset contains 100,000 ratings from 943 users on 1682 movies. This project performs various tasks using Spark SQL to uncover patterns and answer the following questions:

1. **Average rating for each movie**.
2. **Top 10 movies with the highest average ratings**.
3. **Users who have rated at least 50 movies and their favorite movie genres**.
4. **Users who are younger than 20 years old**.
5. **Users whose occupation is "Scientist" and whose age is between 30 and 40 years old**.

## Tools & Technologies
![Hadoop Ecosystem](https://img.shields.io/badge/Hadoop%20Ecosystem-660000?style=flat&logo=apache-hadoop&logoColor=white)
![Spark](https://img.shields.io/badge/Apache%20Spark-FF3333?style=flat&logo=apache-spark&logoColor=white)
![Zeppelin](https://img.shields.io/badge/Apache%20Zeppelin-003F7D?style=flat&logo=apache-zeppelin&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-006F9C?style=flat&logo=sql&logoColor=white)

- **Apache Zeppelin**: For interactive data exploration.
- **Apache Spark SQL**: For querying and processing the dataset.
- **ML-100k Dataset**: The dataset used for analysis.

## Dataset

- `u.data`: Ratings data (userID, movieID, rating, timestamp).
- `u.item`: Movie data (movieID, title, genre).
- `u.user`: User data (userID, age, gender, occupation, zip code).

## Tasks Performed

1. **Calculate the average rating for each movie**:
   - Aggregate the ratings for each movie and calculated the average.

2. **Identify the top 10 movies with the highest average ratings**:
   - Sort the movies based on their average ratings in descending order.

3. **Find the users who have rated at least 50 movies and their favourite genres**:
   - Filter users who have rated 50 or more movies, then identified their favorite movie genres based on their ratings.

4. **Find all the users who are less than 20 years old**:
   - Filter users by age to identify those younger than 20.

5. **Find all the users whose occupation is "scientist" and whose age is between 30 and 40 years old**:
   - Filter users based on occupation and age range.

## Setup Instructions

### Prerequisites:
1. **Hadoop Ecosystem**: Make sure the hadoop ecosystem is set up.
1. **Apache Zeppelin**: Make sure Apache Zeppelin is installed and running.
2. **Spark**: Ensure Spark is installed and configured with Zeppelin.


### Steps to run the project:

1. Clone the repository or download the necessary files from the MovieLens dataset.
2. Open Apache Zeppelin and upload the JSON file into your notebook
3. Run the dataset accordingly,

> Extra Feature: There is a shell script included in the notebook to get the dataset

```shell
wget http://media.sundog-soft.com/hadoop/ml-100k/u.user -O /tmp/u.user
wget http://media.sundog-soft.com/hadoop/ml-100k/u.data -O /tmp/u.data
wget http://media.sundog-soft.com/hadoop/ml-100k/u.item -O /tmp/u.item
```
