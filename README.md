Title: Predictive Anomaly Detection of the Air Production Unit (APU) failure

Objective: 
- To simulate real time data streaming of signals, design a data pipeline and proceed streaming integration with Kafka connect.
- To predict anomaly detection using traditional machine learning methods (Offline) and Online machine learning.

Steps to run the source codes:

1. Download the zip files for further usage.
2. Download raw data from this link via https://archive.ics.uci.edu/dataset/791/metropt+3+dataset and save the file as 'data.csv'.
3. Move the file named 'data.csv' into the targeted folder.
4. Run docker to generate required features.
5. Run Producer, Curl, Consumer and Streamlit respectively. Codes to run each stage are in both Producer and Consumer files.

Else, please see the codes required to run Producer, Curl, Consumer and Streamlit below.
1. Producer: python avro_producer.py -b "localhost:9092" -t "AIRPOLL" -s "http://localhost:8081"
2. Curl: curl -d @"sinkMysql_airpoll.json" -H "Content-Type: application/json" -X POST http://localhost:8083/connectors
3. Consumer: python avro_consumer.py -b "localhost:9092" -s "http://localhost:8081" -t "AIRPOLL" -g "air"
4. Streamlit: streamlit run app.py
