FROM tomcat:9.0.44-jdk8

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y git && \
    apt-get install -y maven

RUN git clone https://github.com/db-ee/ontop-spatial.git -b diststrabon 

WORKDIR "/usr/local/tomcat/ontop-spatial"

COPY dictionary.csv ./
COPY statistics.csv ./
COPY asWKTTables.txt ./

COPY connection.properties ./endpoint-livy/WebContent/WEB-INF/

RUN mvn clean install -DskipTests

RUN mv ./endpoint-livy/target/endpoint2-livy-1.16.1.war /usr/local/tomcat/webapps/
