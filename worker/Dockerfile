FROM maven:3.8.4-jdk-11-slim as builder

WORKDIR /home/popeye/worker/build

COPY pom.xml .

RUN mvn dependency:resolve

COPY . .

RUN mvn package

FROM openjdk:11-jre-slim as run

WORKDIR /home/popeye/worker/run

COPY --from=builder /home/popeye/worker/build/target/*.jar ./

CMD ["java", "-jar", "worker-jar-with-dependencies.jar"]
