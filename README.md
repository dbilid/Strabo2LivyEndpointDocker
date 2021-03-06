Dockerfile for Strabo2 Livy Endpoint

Jars from strabo2docker/geospark must be put in a directory in the host machine, accessible by Livy, e.g. /tmp/, and value sparkJars in connection.properties must be updated accordingly.

Docker container can be built as:

docker image build -t NAME DIR

where NAME is an appropriate name and DIR the directory that contains the Dockerfile

Docker container can be executed as:

docker container run -it --publish PORT:8080 NAME

where PORT should be replaced by an appropriate port number and NAME is the name given in the build command.
After launching, the endpoint will be available at http://IP:PORT/endpoint2-livy-1.16.1/

File connection.properties must be modified according to the Livy setup. Each entry in connection.properties can also be passed as environment variable. In this case the value of connection.properties is overwriten by the environment variable. (For example run the docker container as follows in order to overwrite the databaseName from the connection.properties: docker container run -it --publish PORT:8080 --env databaseName=DBNAME NAME. The key MUST be present in connection.properties in order to be taken into consideration when reading the environment variables.

Files statistics.csv, dictionary.csv and asWKTTables.txt are dataset specific and are produced by the Strabo2 loader.
