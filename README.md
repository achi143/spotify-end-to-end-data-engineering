# Spotify End-To-End data Engineering

### Introduction
Built an End-to-End ETL pipeline using the Spotify API on AWS The pipeline will retrieve data from the spotify API, transform it using Python, and load it into AWS cloud storage.
### About Dataset/API
This API contains information about music artist, album and songs- [Spotify API] (https://developer.spotify.com/documentation/web-api)
### Services Used
1. **S3 (Simple Storage Service):** Amazon S3 (Simple Storage Service) is highly scalable object storage service that can store and retrieve any amount of data from anywhere on the web. It is commonly used to store      and distribute large media files, data backups, and static website files.
2. **AMS Lambda:** AMS Lambda is a serverless computing service that lets you run your code without managing servers. You can use Lambda to run code in esponse to events Like changes in S3, DynamoDB, or other ANS         services.
3. **Cloud Watches:** Amazon Cloudwatch is a monitoring service for ANS resources and the applications you run on them. You can use Cloudwatch track metrics, collect and monitor log files, and set alarms.
4. **Glue Crawler:** AWS Glue Crawler is a fully managed service that automatically crawls your data sources, identifies data formats and infers schemas, and creates tables in the AWS Glue Data Catalog.
5. **Data Catalog:** AWS Glue Data Catalog 1s a fully managed metadata repository that makes it easy to discover and manage data in AWS you can use the Glue Data Catalog with other AWS services, such as Athena.
6. **Amazon Athena:** Anazon Athena is an interactive query service that makes it easy to analyze data in Anazon S3 using standard SQL you can Athena to analyze data in your Glue Data Catalog or in other S3 buckets.

### Install Packages 
```
pip install pandas.
pip install numpy.
pip install spotipy.
```

### Project Execution Flow
Extract Data from API -> Lambda Trigger (every 1 hour) -> Run Extract code -> Store Raw Data -> Trigger Transform Function -> Transform Data and Load it -> Query Using Athena. 
