# Data Lake using Spark

by Kallibek Kazbekov

Date: 3/26/2021
---
# Project summary

## Purpose

This project offers an ETL process for an imaginary music streaming startup called Sparkify to move their data warehouse to a data lake using Spark. Their data resides in S3, in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

## ETL

The code builds an ETL pipeline that extracts their data from S3, processes them using Spark, and loads the data back into S3 as a set of dimensional tables. This will allow their analytics team to continue finding insights in what songs their users are listening to.

# Project instructions on how to run the Python scripts

Before executing the code, make sure to set your AWS credentials (access key ID  and secret access key) in the `dl.cfg` file.

To execute the code type `python etl.py` in the terminal and press 'Enter'

# An explanation of the files in the repository

## `etl.py`

```python

def main():
    """
    First, the function initiates a spark session.
    Then, performs an ETL process for the song and log data.
    Each ETL extracts data from json files stored on a public S3 bucket, 
    transforms data into a star schema and loads into an S3 bucket for analytics purposes. 
    """
    
def create_spark_session():
    """Creates and returns a spark session."""

def process_song_data(spark, input_data, output_data):
    """
    Does ETL process for the song data.
    
    ETL consists of three stage:
    1) Extract - reads song data stored in JSON in a S3 bucket 
    2) Transform - extracts columns to create songs and artists tables
    3) Load - saves dimentional tables (songs and artists) to an S3 bucket as parquet files. 
    """
    
def process_log_data(spark, input_data, output_data):
    """
    Does ETL process for the song data.
    
    ETL consists of three stage:
    1) Extract - reads log data stored in JSON in a S3 bucket 
    2) Transform - extracts columns to create users, datetime, and songplays tables
    3) Load - saves tables to an S3 bucket as parquet files. 
    """
```    
## `dl.cfg`

The file contains AWS credentials (access key ID  and secret access key) for programmatic access to AWS services.

AWS_ACCESS_KEY_ID=''

AWS_SECRET_ACCESS_KEY=''
