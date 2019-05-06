# Producer-Consumer
Producer consumer home task for BigPanda.

Before you run the project:
1. Use Maven to get all libraries which are in use (imported) by this project – the dependencies.
2. Make sure that the "EventsSource.txt" file is located at the main directory of the package (the same directory as the pom.xml file). 
   The content of this file represents the source of the event data (the output of the blackbox).

How to run the project:
1. The ProducerConsumer project contains 3 Java classes at src/main/java/producerConsumer package.
2. In order to run the project, run the “ServicePoc” class, it contains the main() method. 
3. A good run will display the statistical information on the event type and the data, as refer to the event data at the "EventsSource.txt" file.

Future improvements:
1. Display the statistical information periodically in predefined intervals, using the method (StatsSubscriber) displayStatistics(). 
   But not only when the Observable send onCompleted notification to the Subscriber, as it is today.   
2. Consider using a publish-subscrib messaging system (e.g. Apache Kafka) in the middle between the observer and the subscriber. 
   It will handle better a situation of large scale data, with more reliability and with less data loss.
3. Consider using several subscribers in parallel, by concurrent threads, 
   in order to handle better with a pressure of large scale event data.
