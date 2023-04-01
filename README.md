# CS348 Group Project

This application is based on datasets of movies and TV shows and allows movie and TV show fans to search, view, rate and leave comments for each movie and TV show.

# SQL
## Create the database
SQL Database is created by [sql/initial.sql](sql/initial.sql), which is used for creating tables, constraints, and stored triggers.
1. Go to the `sql` folder.
1. In the MySQL server, run the initial.sql by `source initial.sql;`.  This will create a new database called `CS348_Movie_DB` and all the tables needed and create a user with the name 'user1' and password 'Password0!'.

## Load the sample database
Sample database  [sql/sample-data.sql](sql/sample-data.sql) is generated by [scripts/scrapy_top10.py](scripts/scrapy_top10.py), you can recreate it by running `python3 scripts/scrapy_top10.py`. You need to install the python package `cinemagoer` by running `pip install cinemagoer` to scrape the data.
1. Type `source initial.sql;` to initialize the database.
1. Type `source sample-data.sql;` to load the sample dataset.
1. Type `source test-sample.sql;` to test the 6 functionalities on the sample dataset.

## Load the production database
Production database [sql/production-data.sql](sql/production-data.sql) is generated by [scripts/scrapy_top250.py](scripts/scrapy_top250.py), you can recreate it by running `python3 scripts/scrapy_top250.py`. You need to install the python package `cinemagoer` by running `pip install cinemagoer` to scrape the data.
1. Type `source initial.sql;` to initialize the database.
1. Type `source production-data.sql;` to load the production dataset.
1. Type `source test-production.sql;` to test the 6 functionalities on the production dataset.

## Functionalities
1. View information about the movie selected based on the name. (ex. `The Lord of the Rings`)
2. Find all movies with ratings in a specific range. (ex. `> 7.0/10.0`)
3. Order all movies by their rate order. (ex. `High-to-Low` or `Low-to-High`)
4. Find movies with `top-n` ratings. (ex. `n <= 10`)
5. Leave both a rating and a comment on a specific movie.
6. Update the given rate and comments based on the user name.

# Data-driven application
Before running the data-driven application, please be sure to load in databases (sample or production).
## Installation
1. Go to the `back-end` folder,
    1. type ` pip install -r requirements.txt ` to install all python packages,
    2. and type `python3 main.py` to start.
2. Go to the `front-end` folder,
    1. type `npm install` to install dependencies,
    2. In the same folder, type `npm start`, and this will display a webpage.
    
## Functionalities
1. View information about the movie selected based on the name. (ex. `The Lord of the Rings`)
2. Find all movies with ratings in a specific range. (ex. `> 7.0/10.0`)
3. Order all movies by their rate order. (ex. `High-to-Low` or `Low-to-High`)
4. Find movies with `top-n` ratings. (ex. `n <= 10`)

## Instruction For Running
1. [Initialize database](#create-the-database)
2. [Load Data](#load-the-production-database)
3. [run main.py in back-end folder](#installation)
4. [npm start in front-end folder](#installation)
5. Go to website localhost:3000

# Members
Claire Sheng

Ganlin Feng

Junyi Liu

Yuming Long
