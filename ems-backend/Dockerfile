# Use a slim and secure Java runtime as the base image
FROM eclipse-temurin:17-jre-jammy

# Set the working directory inside the container
WORKDIR /app

# Copy the executable JAR file from the build stage to the container
# Replace 'your-app-name-0.0.1-SNAPSHOT.jar' with the actual name of your JAR file
COPY target/ems-backend-0.0.1-SNAPSHOT.jar app.jar

# Expose the port the app runs on (Render will map this)
EXPOSE 8080

# The command to run the application
ENTRYPOINT ["java", "-jar", "app.jar"]

