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
