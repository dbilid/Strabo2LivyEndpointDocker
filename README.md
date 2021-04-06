Dockefile for Strabo2 Livy Endpoint

Docker container can be built as:

docker image build -t NAME DIR

where NAME is an appropriate name and DIR the directory that contains the Dockerfile

Docker container can be executed as:

docker container run -it --publish PORT:8080 NAME

where PORT should be replaced by an appropriate port number and NAME is the name given in the build command.
After launching, the endpoint will be available at http://IP:PORT/endpoint2-livy-1.16.1/

File connection.properties must be modified according to the Livy setup.

Files statistics.csv, dictionary.csv and asWKTTables.txt are dataset specific and are produced by the Strabo2 loader.
