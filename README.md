[![Build Status](https://travis-ci.org/systelab/config-service.svg?branch=master)](https://travis-ci.org/systelab/config-service)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/7ce4e563c45b4d09a975d61bed7d5d50)](https://www.codacy.com/app/systelab/config-service?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=systelab/config-service&amp;utm_campaign=Badge_Grade)
[![Known Vulnerabilities](https://snyk.io/test/github/systelab/config-service/badge.svg?targetFile=pom.xml)](https://snyk.io/test/github/systelab/config-service?targetFile=pom.xml)

#  Configuration Service

Configuration service to manage external properties for applications across all environments. Configurations are stored at https://github.com/systelab/config-service-repository

## Getting Started

To get you started you can simply clone the `config-service` repository and install the dependencies:

### Prerequisites

You need [git][git] to clone the `config-service` repository.

You will need [Java™ SE Development Kit 8][jdk-download] and [Maven][maven].

### Clone `config-service`

Clone the `config-service` repository using git:

```bash
git clone https://github.com/systelab/config-service.git
cd config-service
```

### Install Dependencies

In order to install the dependencies and generate the Uber jar you must run:

```bash
mvn clean install
```

### Run

To launch the server, simply run with java -jar the generated jar file.

```bash
cd target
java -jar config-service-1.0.jar
```

Head to http://localhost:8888/patient-service.yml or http://localhost:8888/patient-service/default to get a sample configuration

Check the repository at https://github.com/systelab/config-service-repository for more available configurations

## Docker

### Build docker image

There is an Automated Build Task in Docker Cloud in order to build the Docker Image. 
This task, triggers a new build with every git push to your source code repository to create a 'latest' image.
There is another build rule to trigger a new tag and create a 'version-x.y.z' image

You can always manually create the image with the following command:

```bash
docker build -t systelab/config-service . 
```

### Run the container

```bash
docker run -p 8888:8888 systelab/config-service
```



[git]: https://git-scm.com/
[sboot]: https://projects.spring.io/spring-boot/
[maven]: https://maven.apache.org/download.cgi
[jdk-download]: http://www.oracle.com/technetwork/java/javase/downloads
[JEE]: http://www.oracle.com/technetwork/java/javaee/tech/index.html
