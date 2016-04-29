# monitor-stat-kafka

Create a monitor system which report realtime statistics  using Java, Kafka and Graphite

Language: Java  
Data feeding :  Kafka  
Metrics dashboard:  Grafana   
Chart:  Graphite  


##Kafka
Apache Kafka is an open-source message broker project developed by the Apache Software Foundation written in Scala. The project aims to provide a unified, high-throughput, low-latency platform for handling real-time data feeds.  
The design is heavily influenced by transaction logs.

###Key features
- Producer 
- Consumer
- Topic
- Partition
- Consumer fetcher 
- Replication 
- Offset


###Kafka usage Notes
- More Partitions Lead to Higher Throughput (but consume more memory) 
- Message size should be small (1kb), larger messages (for example, 10 MB to 100 MB) can decrease throughput and significantly impact operations.
- A cluster should have at least 3 machines, otherwise, stay with standalone node instead (with SSD or multidisks for better performance).
- Use high level consumer with default(1) thread setting if possible. Use G1 Collector -XX:+UseG1GC


##[Scribe](https://github.com/facebookarchive/scribe)
Scribe is a server for aggregating log data that’s streamed in real time from clients. It is designed to be scalable and reliable.

##[Grafana](http://grafana.org)
An open source, feature rich metrics dashboard and graph editor for Graphite, InfluxDB, OpenTSDB.

##[Graphite](https://graphite.readthedocs.org/en/latest/)
Scalable Realtime Graphing.  
