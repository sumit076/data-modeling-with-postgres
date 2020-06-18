# Data Modeling with Postgres

## Introduction

The goal of this project is to build a PostgreSQL database utilizing the data on users activity and songs metadata. Building the database helps us do complex analytics regarding users activity as well as song play analysis.

## Data

The songs' metadata sourse is a subset of the [Million Song Dataset](https://labrosa.ee.columbia.edu/millionsong/). Also, the users' activities is a simulated data using [eventsim](https://github.com/Interana/eventsim). The data resides in two main directories:

- Songs metadata: collection of JSON files that describes the songs such as title, artist name, year, etc.
- Logs data: collection of JSON files where each file covers the users activities over a given day.

## Methodology

We'll build the database by optimizing the tables around efficient reads for complex queries. To do that, **Star** schema will be used utilizing dimensional modeling as follows:

- Fact table: songplays.
- Dimensions tables: songs, artist, users, time.

![](star_schema.jpg)
