Hello Testing
# Overview
This project aims to buil an ETL pipeline that extracts their data from S3, processes them using Spark, and loads the data back into S3 as a set of dimensional tables.


## Introduction
To complete the project, firstly, should load data from S3, process the data into analytics tables using Spark, and load them back into S3. Then  deploy this Spark process on a cluster using AWS.

## Data set
The first dataset is a subset of real data from the Million Song Dataset. Each file is in JSON format and contains metadata about a song and the artist of that song. The files are partitioned by the first three letters of each song's track ID. For example, here are filepaths to two files in this dataset.

```
song_data/A/B/C/TRABCEI128F424C983.json
song_data/A/A/B/TRAABJL12903CDCF1A.json
````

```
{"num_songs": 1, "artist_id": "ARJIE2Y1187B994AB7", "artist_latitude": null, "artist_longitude": null, "artist_location": "", "artist_name": "Line Renaud", "song_id": "SOUPIRU12A6D4FA1E1", "title": "Der Kleine Dompfaff", "duration": 152.92036, "year": 0}

```


The log files in the dataset you'll be working with are partitioned by year and month. For example, here are filepaths to two files in this dataset.
```
log_data/2018/11/2018-11-12-events.json
log_data/2018/11/2018-11-13-events.json
```

## Code
* process_song_data: This function loads song_data from S3 and deals with it by extracting the songs and artist tables  and then again loaded back to S3

* process_log_data: This function loads log_data from S3 and deals with it by extracting the songs and artist tables
        and then again loaded back to S3. Also output from previous function is used in by spark.read.json command

