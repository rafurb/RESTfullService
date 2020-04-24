FROM openjdk:8-jdk-alpine
ARG JAR_FILE=target/*.jar
RUN addgroup -S spring && adduser -S spring -G spring 
USER spring:spring
COPY ${JAR_FILE} app.jar
ENTRYPOINT ["java", "-jar", "/app.jar"]
EXPOSE 8080