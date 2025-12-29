# Use Java 17
FROM eclipse-temurin:17-jdk

# Set working directory
WORKDIR /app

# Copy project files
COPY mvnw .
COPY .mvn .mvn
COPY pom.xml .
COPY src ./src

# Give execute permission for Maven wrapper
RUN chmod +x mvnw

# Build the Spring Boot app (skip tests for faster build)
RUN ./mvnw clean package -DskipTests

# Expose port 8082
EXPOSE 8082

# Run the JAR file
CMD ["sh", "-c", "java -jar target/*.jar"]
