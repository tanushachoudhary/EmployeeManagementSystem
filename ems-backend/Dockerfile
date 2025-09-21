# ---- Stage 1: Build the application ----
# Use a Maven image to build the project
FROM maven:3.8-eclipse-temurin-17 AS build

WORKDIR /app

# Copy the pom.xml and download dependencies first for caching
COPY pom.xml .
RUN mvn dependency:go-offline

# Copy the rest of the source code and build the application
COPY src ./src
RUN mvn package -DskipTests

# ---- Stage 2: Create the final, smaller image ----
# Use a slim Java runtime image for the final product
FROM eclipse-temurin:17-jre-jammy

WORKDIR /app

# Copy the JAR file from the 'build' stage
# IMPORTANT: Replace this with your actual JAR file name
COPY --from=build /app/target/ems-backend-0.0.1-SNAPSHOT.jar app.jar

EXPOSE 8080

ENTRYPOINT ["java", "-jar", "app.jar"]
