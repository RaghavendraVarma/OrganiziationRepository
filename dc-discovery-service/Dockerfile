# Start with a base image containing Java runtime
FROM khipu/openjdk17-alpine

# Add Maintainer Info
LABEL maintainer="lakshman@socialtalentagency.com"

# Add a volume pointing to /tmp
VOLUME /tmp

# Make port 8001 available to the world outside this container
EXPOSE 9091

# The application's jar file
ARG JAR_FILE=target/*.jar

# Add the application's jar to the container
ADD ${JAR_FILE} discovery-service.jar

# Run the jar file 
ENTRYPOINT ["java","-Dspring.profiles.active=${ENV}","-jar","/discovery-service.jar"]