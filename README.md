# Stock-Market-PubSub-Realtime-Analytics-Project


![Streaming Architecture (1)](https://user-images.githubusercontent.com/104515955/235704164-20334cb8-17af-4933-98e4-e0b3cc2c709a.JPG)


# Google Secret Manager 
 Secret Manager is a secure and convenient storage system for API keys, passwords, certificates, and other sensitive data. Secret Manager provides a central place and single source of truth to manage, access, and audit secrets across Google Cloud. Here I have stored my API key securely.

# Publisher 
 Publisher code is used to pull data from the API, transform and stream as JSON to Pub Sub topic. I have also fetched the API key securely from Google Secret Manager.

# Subscriber 
 Subscriber code is responsible for loading the stream to Bigquery table. also the messages are acknowledged to free up the subscriber.

# Cloud Pub Sub 
Pub/Sub is used for streaming analytics and data integration pipelines to ingest and distribute data. It's equally effective as a messaging-oriented middleware for service integration or as a queue to parallelize tasks. Pub/Sub enables you to create systems of event producers and consumers, called publishers and subscribers.
  

# Bigquery 
Bigquery is a serverless centralized datawarehouse to store,manipulated data. It is also used to create ML models. Here I'm storing events of data for further analytics. 

# Powerbi 
Power BI is a unified, scalable platform for self-service and enterprise business intelligence (BI). Connect to and visualize any data.


# Process involved
I created a streaming pipeline to fetch data in real-time from Alpha Vantage API to transform data to JSON format which can be readily inserted to Bigquery, then publish it to Pub Sub topic.

Once the stream flows to the topic, it consumed, loaded to Bigquery and the message is acknowledged. On top of my table is view is created. The stream of data in my view is connected live to Bigquery view above which dashboard is created where data is visualized and analytics is performed. Also had an idea of using Looker, but couldn't use in free trial.

Moreover, I have used  Google Secret Manager to secure my API key and utilized it in publisher. 



