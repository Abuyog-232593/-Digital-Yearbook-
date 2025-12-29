# Use Java 17
FROM eclipse-temurin:17-jdk

# Set working directory
WORKDIR /app

# Copy only necessary files
COPY mvnw .
COPY .mvn .mvn
COPY pom.xml .
COPY src ./src

# Build the Spring Boot app
RUN ./mvnw clean package -DskipTests

# Expose port your app will run on
EXPOSE 8082

# Automatically find the JAR in target/ and run it
CMD java -jar $(ls target/*.jar | head -n 1)
