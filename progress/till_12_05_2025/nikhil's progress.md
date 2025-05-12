#  Nikhil's Progress 



1. Setup Server for API using flask and deployed it as a public URL using **ngrok**

## Setting up Context for DDOS Agent specifically 

- Created a tool for capturing Global metrics within a pre-defined window ( for example capturing the numbers of requests from a certail IP within a period of 60 seconds , as context for the LLM and parameters for the deep learning model ) 

![image](image.png)

## Setting up entire Agent workflow for ease of use 
- created a common Agent class for ease of use and live updates on processes 
- created a POST request handler for the incoming traffic logs 
- working on the formatting functions required to convert the incoming POST request payload into Model usable input 
- current input to the API includes the following parameters
### Request format 
```
- tcp source port 
- tcp destination port 
- ip length 
- payload length
- ip ttl 
- ip tos
- tcp data offset
- tcp flags(as integers)
- payload bytes 
- Ip
- country 
- User agent
- ASN 
- HTTP Method
- cookies
- headers
```