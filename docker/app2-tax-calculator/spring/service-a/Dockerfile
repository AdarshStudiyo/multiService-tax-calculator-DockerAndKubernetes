FROM eclipse-temurin:25-jdk
WORKDIR /app
COPY target/*.jar app.jar
EXPOSE 3000
CMD [ "java","-jar","app.jar","--server.port=3000" ]