kibana-jetty
============

A simple pom file that will download and unpack Kibana, then wrap it in a war.

Run:
 mvn clean install
 mvn cargo:run
 
Then access the kibana console from http://localhost:8080/kibana-jetty/kibana-3.0.0milestone4
