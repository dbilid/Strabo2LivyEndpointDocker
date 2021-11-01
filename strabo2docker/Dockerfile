FROM tomcat:9.0.44-jdk8

WORKDIR "/usr/local/tomcat/ontop-spatial"

RUN wget godel.di.uoa.gr:8080/endpoint2-livy-1.16.1.war

RUN mv ./endpoint2-livy-1.16.1.war /usr/local/tomcat/webapps/

COPY dictionary.csv ./
COPY statistics.csv ./
COPY asWKTTables.txt ./

COPY connection.properties ./../webapps/

COPY logging.properties ./../../conf/
