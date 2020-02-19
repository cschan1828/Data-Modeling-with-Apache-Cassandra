# Data Modeling with Apache Cassandra
## Introduction
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to. Currently, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

Consequently, a data engineer is required to create a Cassandra database which can create queries on song play data to answer the questions and discover business values. My role is to design a database schema and ETL pipeline for this analysis.

## Dataset
The first dataset is a subset of real data from the [Million Song Dataset](https://labrosa.ee.columbia.edu/millionsong/). Each file is in csv format and contains metadata about events. The files are partitioned by date.

## Model a Apache Cassandra database
In this project, Apache Cassandra database is adopted. For such database, denomrialization must be doen for fast read. Additionally, model the data before query is required. That is, our strategy is one table per query.

## Relevant Files
* Cassandra_ETL.ipynb: Read csv files, process and load them into database.
