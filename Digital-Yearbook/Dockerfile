# Use Java 17
FROM eclipse-temurin:17-jdk

# Set working directory
WORKDIR /app

# Copy Maven wrapper and project files
COPY . .

# Build the Spring Boot app
RUN ./mvnw clean package -DskipTests

# Expose port used by Spring Boot
EXPOSE 8082

# Run the app
CMD ["java", "-jar", "target/*.jar"]
