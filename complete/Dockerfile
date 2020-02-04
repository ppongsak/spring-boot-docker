# FROM openjdk:8-jdk-alpine
# ARG JAR_FILE=target/*.jar
# COPY ${JAR_FILE} app.jar
# ENTRYPOINT ["java","-jar","/app.jar"]

# FROM adoptopenjdk/openjdk12:ppc64le-ubi-minimal-jre-12.0.2_10

FROM adoptopenjdk
COPY target/*.jar /root
COPY env/meekycvit.properties /root/p.properties

WORKDIR /root

CMD ["java", "-jar", "-Dfile.encoding=UTF-8", "gs-spring-boot-docker-0.1.0.jar", "--spring.config.location=file:///root/p.properties", "&"]