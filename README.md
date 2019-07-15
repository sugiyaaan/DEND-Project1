# Project1: Data Modeling with Postgres
***
1. The purpose of this database and analytical goals.

A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. 
The analytics team is particularly interested in understanding what songs users are listening to.
Currently, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

They'd like a data engineer to create a Postgres database with tables designed to optimize queries on song play analysis, and bring you on the project. 
Your role is to create a database schema and ETL pipeline for this analysis. You'll be able to test your database and ETL pipeline by running queries given to you by the analytics team from Sparkify and compare your results with their expected results.


2. Database schema design and ETL pipeline.
### Fact Table
* songplays - records in log data associated with song plays i.e. records with page NextSong
* songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent
### Dimension Tables
* users - users in the app
* user_id, first_name, last_name, gender, level
* songs - songs in music database
* song_id, title, artist_id, year, duration
* artists - artists in music database
* artist_id, name, location, lattitude, longitude
* time - timestamps of records in songplays broken down into specific units
* start_time, hour, day, week, month, year, weekday

3. Example queries and results for song play analysis.

4. Song Dataset
The first dataset is a subset of real data from the *[Million Song Dataset](https://labrosa.ee.columbia.edu/millionsong/)*.
Each file is in JSON format and contains metadata about a song and the artist of that song. 
The files are partitioned by the first three letters of each song's track ID. For example, here are filepaths to two files in this dataset.

## how to start the project
1. Execute "create_tables.py". This willto create your database and empty tables.
2. Execute "etl.py". This will build ETL Pipeline.
