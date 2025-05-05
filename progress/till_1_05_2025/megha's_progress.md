#Megha's progress

As part of our security enhancement efforts, I developed a rule generation system designed to detect and block suspicious HTTP requests. 
The rules are generated dynamically based on traffic analysis and can be integrated into Web Application Firewalls (WAFs) for real-time threat mitigation.

Sample Generated WAF Rule:

{
  "type": "WAF Rule",
  "rule_name": "Block Suspicious Request",
  "action": "Block",
  "place_at": "Last",
  "reason": "Malicious HTTP Request Detected by ShieldNet",
  "request": "From 192.168.1.2 to 192.168.1.10 on port 80 using HTTP",
  "timestamp": "2025-05-02 07:15:20.375649"
}
This rule was generated after analyzing HTTP logs.
The system detected a potentially malicious request and triggered a rule to block the traffic accordingly.
These rules can be added to a WAF dashboard for enforcement.

Anomaly Detection - Isolation Forest Model

In parallel, I trained an anomaly detection model using the CIC-IDS 2017 dataset, which contains a wide range of benign and malicious network traffic patterns.
The goal was to build a machine learning model capable of detecting abnormal behavior in web traffic that might indicate attacks like DoS, DDoS, infiltration, or data exfiltration.

Model Training:
Dataset Used: CIC-IDS 2017 (with 225,745 records and 85 features)

Preprocessing:

Dropped missing values

Selected 80 numeric features for model input

Algorithm: Isolation Forest (unsupervised anomaly detection)

Model Output: pulsesense_isolation_forest.pkl
This model is capable of flagging anomalous patterns in WAF traffic, which can be used for alerting or automated response.

