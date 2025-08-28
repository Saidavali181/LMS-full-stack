# Use Java 21 base image
FROM eclipse-temurin:21-jdk-jammy

# Set work directory
WORKDIR /app

# Copy Maven build file and source
COPY pom.xml .
COPY src ./src

# Build the application
RUN ./mvnw clean package -DskipTests

# Expose port
EXPOSE 8085

# Run the JAR
ENTRYPOINT ["java","-jar","target/library-management-0.0.1-SNAPSHOT.jar"]
