# Use Java 17
FROM eclipse-temurin:17-jdk

# Set working directory
WORKDIR /app

# Copy necessary files
COPY mvnw .
COPY .mvn .mvn
COPY pom.xml .
COPY src ./src

# Build the app
RUN ./mvnw clean package -DskipTests

# Expose the port your app will run on
EXPOSE 8082

# Run the app (auto-detect JAR)
CMD java -jar $(ls target/*.jar | head -n 1)
