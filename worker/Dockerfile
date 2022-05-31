FROM maven:3.6.1-jdk-8-alpine

WORKDIR /app

COPY . .

RUN mvn package -DskipTests && \
    mvn target/worker-jar-with-dependencies /run/worker.jar && \
    rm -f *

CMD java -jar /run/worker.jar
