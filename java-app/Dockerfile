# You can change this base image to anything else
# But make sure to use the correct version of Java

FROM adoptopenjdk/openjdk11:alpine-jre

# Simply the artifact path

ARG artifact=target/*.jar 

WORKDIR /app

COPY ${artifact} /app.jar

# Create a non-root user (jenkins) and set the permissions
RUN addgroup -S jenkins && adduser -S jenkins -G jenkins
RUN chown jenkins:jenkins /app.jar

RUN ls -l /app.jar

USER jenkins

# This should not be changed

ENTRYPOINT ["java", "-jar", "app.jar"]