FROM eclipse-temurin:17-jre
WORKDIR /app #workdir
RUN groupadd -r pharma && useradd -r -g pharma pharma
COPY target/*.jar app.jar
USER pharma
EXPOSE 8081
# Launch supplier/auth/catalog microservice as Spring Boot executable JAR
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","app.jar"]
#Auth Service

