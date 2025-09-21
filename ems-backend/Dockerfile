# ---- Stage 1: Build the application ----
# This image for the build stage is correct and available
FROM maven:3-eclipse-temurin-24 AS build

WORKDIR /app

# Copy the pom.xml and download dependencies
COPY pom.xml .
RUN mvn dependency:go-offline

# Copy the source code and build the application
COPY src ./src
RUN mvn package -DskipTests

# ---- Stage 2: Create the final, smaller image ----
# CORRECTED: Use the generic '24-jdk' tag, which is verified to exist.
FROM eclipse-temurin:24-jdk

WORKDIR /app

# Copy the JAR file from the 'build' stage
# Replace 'your-app-name-0.0.1-SNAPSHOT.jar' with your actual JAR file name
COPY --from=build /app/target/your-app-name-0.0.1-SNAPSHOT.jar app.jar

EXPOSE 8080

ENTRYPOINT ["java", "-jar", "app.jar"]
