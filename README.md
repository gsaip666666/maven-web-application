Dockerfile:

# Use Tomcat 9 with Java 21
FROM tomcat:9.0-jdk21-temurin

# Copy the generated WAR file into Tomcat
COPY target/*.war /usr/local/tomcat/webapps/ROOT.war

# Expose Tomcat port
EXPOSE 8080

# Start Tomcat
CMD ["catalina.sh", "run"]
