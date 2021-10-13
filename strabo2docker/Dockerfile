FROM tomcat:9.0.44-jdk8

WORKDIR "/usr/local/tomcat/ontop-spatial"

COPY FoodSecurity1.war /usr/local/tomcat/webapps/

COPY dictionary.csv ./
COPY statistics.csv ./
COPY asWKTTables.txt ./

COPY connection.properties ./../webapps/
