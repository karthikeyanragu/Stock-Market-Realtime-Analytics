# Stock-Market-PubSub-Realtime-Analytics-Project

#google_secret_manager - to secure and use my API key

#publisher - to pull and transform the data from API

#subscriber - to acknowledge and load the data to the target

#cloud_pubsub - to ingest events of streaming 

#bigquery - to store transformed stream of data

#powerbi - to analyze and forecast predictions  



I created a streaming pipeline to fetch data in real-time from Alpha Vantage API to transform data to JSON format which can be readily inserted to Bigquery, then publish it to Pub Sub topic.



Once the stream flows to the topic, it consumed, loaded to Bigquery and the message is acknowledged. On top of my table is view is created. The stream of data in my view is connected live to Power BI dashboard where data is visualized and analytics is performed.



Moreover, I have used  Google Secret Manager to secure my API key and utilized it in publisher. 
