# Introduction
Before we dive into writing _Structured Query Language (**SQL**)_ queries, let's take a look at what makes SQL and the databases that utilize SQL so popular.

I think it is an important distinction to say that _SQL is a language_. Hence, the last word of SQ**L** being language. SQL is used all over the place beyond the databases we will utilize in this class. With that being said, SQL is most popular for its interaction with databases. For this class, you can think of a database as a bunch of excel spreadsheets all sitting in one place. Not all databases are a bunch of excel spreadsheets sitting in one place, but it is a reasonable idea for this class.


# Why do data analysts uses SQL?
There are some major advantages to using ***traditional relational databases***, which we interact with using SQL. The five most apparent are:

- SQL is easy to understand.
- Traditional databases allow us to access data directly.
- Traditional databases allow us to audit and replicate our data.
- SQL is a great tool for analyzing multiple tables at once.
- SQL allows you to analyze more complex questions than dashboard tools like Google Analytics.

> You will experience these advantages first hand, as we learn to write SQL to interact with data.

# SQL vs. NoSQL
You may have heard of **NoSQL**, which stands for **_not only SQL_**. Databases using NoSQL allow you to write code that interacts with the data a bit differently than what we will do in this course. These NoSQL environments tend to be particularly popular for web-based data, but less popular for data that lives in spreadsheets the way we have been analyzing data up to this point. One of the most popular NoSQL languages is called [MongoDB](https://www.mongodb.com/). Udacity has a full course on MongoDB that you can take for free [here](https://www.udacity.com/course/data-wrangling-with-mongodb--ud032), but these will not be a focus of this program.

> NoSQL is not a focus for this course, but you might see it referenced in the real world!

# Example
```sql
SELECT account_id, 
       occurred_at, 
       standard_qty,
       gloss_qty,
       poster_qty,
FROM orders
WHERE (standard_qty = 0 OR gloss_qty = 0 OR poster_qty = 0)
AND occurred_at >= '2016-10-01';
```

# Why do businesses choose SQL?
1. **Data integrity is ensured** - only the data you want to be entered is entered, and only certain users are able to enter data into the database.
2. **Data can be accessed quickly** - SQL allows you to obtain results very quickly from the data stored in a database. Code can be optimized to quickly pull results.
3. **Data is easily shared** - multiple individuals can access data stored in a database, and the data is the same for all users allowing for consistent results for anyone with access to your database.