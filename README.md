# CSC-724-AnomalyPrediction

#### Summary
This is the implementation of our project "System  Anomaly  Prediction  Using  Memory  Networks" for CSC 724 course.

Contributors: Anupam Godse, Cherukeshi Machan and Shantanu Chandorkar{angodse, cmachan, schando}@ncsu.edu

#### Architecture:
Two real time applications used :
    1. REAL-TIME DATA PROCESSING SYSTEM 
    2. RUBIS ONLINE AUCTION BENCHMARK
    
###### REAL-TIME DATA PROCESSING SYSTEM 
  * Apache Kafka as the streaming platform
  * Multi node multi broker kafka cluster
  * NCSU’s Virtual Computing Lab used
  * Spring-Boot Java Application on one kafka node as a REST interface for clients.
  * Producer emulator as client that streams the data.

###### RUBIS ONLINE AUCTION BENCHMARK
  * Rubis cluster consisting web server, a database server and multiple clients
  * NCSU’s Virtual Computing Lab used
  * Clients  Emulator for workload generator
  * Emulator generate  workload that consist browse requests.
  
###### MONITORING SYSTEM METRICS
  * Collectd daemon is used for collect the system metrics at interval 1 sec.
  * CPU, Memory system metrics are monitored
  * Write_Kafka plugin of collectd is used to send the metrics to prediction server .
  * Faults injected using stress tool
  
#### SetUp Instruction:
  1. Reserve the Virtual machines.
  2. Copy each folders to each machine.
  3. In each machine(KafkaNode1,KafkaNode2,RubisApp,MetricKafka) run the setup.sh command to install all the dependencies.
  4. Change ip address in all the configuration files.
  5. In machines(KafkaNode1,KafkaNode2,MetricKafka) run the start.sh command to start the servers.
  6. In RubisApp machine execute the commands given in the readme file.
  
#### WorkLoad Generation
    1. REAL-TIME DATA PROCESSING SYSTEM : Run kafkaproducerEmulator.py using the command "python kafkaproducerEmulator.py 1"    
    2. RUBIS ONLINE AUCTION BENCHMARK: Inside the RUBiS/Client/ folder run the command "make emulator"
    
#### Fault Injection:
    1. CPULeak: To insert the CPU fault in a system run the command "stress -c 0.3 -i 1  -t 10m" . This will spawn workers for 10 minutes
    2. MemLeak: To insert the memory fault in a system run the command "stress -m 22 -t 10s" . This will spawn workers spinning on malloc()/free() for 10 seconds.

    
    
  


  




