# YouTube Comments Data Pipeline
This project involves scraping YouTube video comments using the YouTube Data API in Python, saving the data as a CSV file, and uploading it to an S3 bucket. The entire process is automated using an Apache Airflow DAG, which runs daily on an EC2 instance.

## Introduction:
This project aims to automate the extraction, transformation, and loading (ETL) of YouTube comments data. The data is scraped using the YouTube Data API, saved as a CSV file, and uploaded to an S3 bucket. An Apache Airflow DAG orchestrates the entire workflow, ensuring that the process runs daily without manual intervention. The Airflow instance is hosted on an Amazon EC2 instance.

## Tech Stack:
Python 3.5+<br/>
Apache Airflow<br/>
AWS Account with S3 bucket<br/>
YouTube Data API key<br/>
Amazon EC2 instance<br/>

## Configuration
1. Obtained "Developer Key" to access Youtube API. Google have provided detailed documentation on API.     
2. Set up free AWS free tier account and launched an EC2 instance with an appropriate instance type (e.g., t2.micro) and        Ubuntu/Debian as the OS.
3. Connected to EC2 instance and installed all dependancies.
   
   ![image](https://github.com/vedasree-kommindala/project_youtube/assets/114097793/046480af-c6a2-4c70-beb2-bee24b54d95b)
   
   Commands to install updates:
   i. sudo yum update<br/>
  ii. sudo yum install python3-pip<br/>
 iii. sudo pip install apache-airflow<br/>
  iv. sudo pip install pandas<br/>
   v. sudo pip install s3fs<br/>
5. Developed code to fetch comments from youtube video - "Google I/O '24 in under 10 minutes" and used pandas to save the   
   data into csv file and finally into s3 bucket.
6. Created a DAG that runs daily and copied into Airflow directory.
7. Accessed airflow web interface through 8080 port and triggered the DAG.

## Results
The automated data pipeline successfully scraped YouTube comments, processed them, and uploaded to an S3 bucket.

![image](https://github.com/vedasree-kommindala/project_youtube/assets/114097793/d8381ea9-c8ad-4a6e-ba1c-47682bab823a)

### Reference
1. https://www.youtube.com/watch?v=q8q3OFFfY6c&list=PLBJe2dFI4sgvQTNNkI3ETYJgNPR4CBpFd&index=3
2. https://developers.google.com/youtube/v3/docs/comments
3. https://www.youtube.com/watch?v=SIm2W9TtzR0

