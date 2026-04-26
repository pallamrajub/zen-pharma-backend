FROM eclipse-temurin:17-jre

WORKDIR /app

RUN groupadd -r pharma && useradd -r -g pharma pharma

COPY --chown=pharma:pharma target/*.jar /app/app.jar

USER pharma

EXPOSE 8086

# Start Spring Boot microservice
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app/app.jar"]]
