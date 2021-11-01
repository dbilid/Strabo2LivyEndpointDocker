FROM tomcat:9.0.44-jdk8

ENV JAVA_OPTS="-XX:PermSize=4096m -XX:MaxPermSize=2048m"

WORKDIR "/usr/local/tomcat/ontop-spatial"

COPY FoodSecurity1.war /usr/local/tomcat/webapps/

COPY dictionary.csv ./
COPY statistics.csv ./
COPY asWKTTables.txt ./

COPY connection.properties ./../webapps/

COPY logging.properties ./../../conf/
RUN ls ./../../conf/
RUN cat ./../../conf/logging.properties
