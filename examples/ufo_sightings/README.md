#UFO Sightings Example

## Building

## Import sample data

To create a collection populated with sample data, use `mongoimport` to read records from the provided JSON file and insert them into a 
mongo collection:

    mongoimport -h localhost -p 27017 -d test -c ufo ./src/main/resources/ufo_awesome.json

## Run Map/Reduce job

To run the job, invoke `hadoop jar` from your hadoop binaries, and provide your input and output URIs.

    $HADOOP_HOME/bin/hadoop jar ./target/ufo-example_cdh4.3.0-1.1.0.jar -Dmongo.input.uri=mongodb://localhost:27017/test.ufo -Dmongo.output.uri=mongodb://localhost:27017/test.ufo_out 


