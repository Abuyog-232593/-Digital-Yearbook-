# Use Java 17
FROM eclipse-temurin:17-jdk

# Set working directory
WORKDIR /app


RUN ./mvnw clean package -DskipTests

EXPOSE 8082

