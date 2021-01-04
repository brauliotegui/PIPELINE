# PIPELINE
A data pipeline to scrape and analyze posts from social media for tracking feedback on a specific product/brand/company.
Data Engineering project set up with Docker, APIs, Airflow, databases, and a BI tool.

## Twitter Metabase Data Pipeline
<img src="https://github.com/brauliotegui/PIPELINE/blob/main/dataflow_diagram.jpg">
<img src="https://github.com/brauliotegui/PIPELINE/blob/main/airflow-demo.gif">
<img src="https://github.com/brauliotegui/PIPELINE/blob/main/metabase-demo.gif">

### Description

This project analyzes the sentiment of tweets on airline companies during a COVID-19 wave to monitor how the customers have been perceiving them throughout this challenging time for these businesses. The tweets are analyzed on an ETL Python script to indicate if they bring a positive or negative sentiment.
This data engineering project is composed of a data pipeline that implements several docker containers organised via docker-compose and managed and scheduled through Apache Airflow.

[Docker](https://www.docker.com/) can package an application and its dependencies in a virtual container that can run on any machine and thus makes deployment much easier.  
[Airflow](https://airflow.apache.org/) is a Python workflow management platform originally developed at Airbnb that is open-source.

### Features

A Dockerized Data Pipeline that stores a stream of Twitter data in databases, analyzes the sentiment of tweets and visualizes the results on a Metabase dahsboard.

* Build an infrastructure of docker containers
* Collect Tweets through Twitter API (airlines as keywords: Ryanair, easyJet, KLM, Lufthansa, TAP, British Airways)
* Store Tweets in a Mongo DB
* Perform sentiment analysis with [vaderSentiment](https://github.com/cjhutto/vaderSentiment) and [Flair](https://github.com/flairNLP/flair)
* Store transformed Tweets in a Postgres database
* Visualize data as [Metabase](https://www.metabase.com/) dashboard

### Usage

* Install docker on your machine
* Clone the repository
* Get credentials for Twitter API and insert them in config.py
* Run docker-compose build, then docker-compose up in terminal
