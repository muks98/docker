FROM openjdk:8-jre-alpine

ENV JAVA_VERSION 1.8.0
ENV MAVEN_VERSION 3.3.9

WORKDIR /app
ADD . /app

EXPOSE 8080

ARG spring_jar=test.jar

LABEL io.k8s.description="Springboot image built from base-centos7 image" \
      io.k8s.display-name="Maven Springboot" \
      io.openshift.tags="builder,java,springboot,java8"

#     echo "$(find / -name java -print)" \
RUN { \
     echo `java -version`; \
    } 

ENTRYPOINT ["java", "-jar", "cryptoapp-final.jar"]
