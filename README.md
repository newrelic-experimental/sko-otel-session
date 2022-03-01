# FY23-SKO OpenTelemetry Session

This repository contains the Java application being used alongside the OpenTelemetry session at SKO-FY23. 

The application in this exercise has been instrumented with OpenTelemetry. Follow the instructions below to run the app using Docker and view the data in New Relic One. 

## Requirements:
In order to participate in this exercise you will need...

* Laptop with Mac OS X, Windows is not supported for this workshop
* [Docker for Mac](https://www.docker.com/products/docker-desktop)
* A New Relic account


## Step 1
Clone this repository to your local machine using `git clone`

## Step 2 
Navigate into the directory you just created and Export your New Relic ingest key using the following command:
```shell
export NEW_RELIC_API_KEY=<your_license_key>
```

## Step 3
Build and run the app using Docker:
```shell
docker-compose up
```

## Step 4
To generate data for this applicaiton, opena new terminal sheell, navigate to the proper directory and run the command below. Note: be sure to update the command to include your ingest license key.
```shell
./load-generator.sh
```

## Step 5 
Head to your New Relic account to view the data coming in! The application named `fibonacci-java` should be found in under `Services - OpenTelemetry` in the left menu of the explorer page

