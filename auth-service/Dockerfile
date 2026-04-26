FROM eclipse-temurin:17-jre
WORKDIR /app #workdir
RUN groupadd -r pharma && useradd -r -g pharma pharma
COPY target/*.jar app.jar
USER pharma
EXPOSE 8081
ENTRYPOINT ["java", "-jar", "-Djava.security.egd=file:/dev/./urandom", "app.jar"]
#Auth Service

