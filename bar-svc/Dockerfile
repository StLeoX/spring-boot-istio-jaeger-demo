FROM chanjarster/openjdk:8-alpine

ARG NAME
ARG VERSION
ARG JAR_FILE

LABEL name=$NAME \
      version=$VERSION
USER root

# 新建用户java-app
RUN  mkdir -p /home/java-app/lib /home/java-app/etc /home/java-app/logs /home/java-app/tmp;


COPY target/bar-svc-0.1.0.jar /home/java-app/lib/app.jar

CMD ["/usr/bin/java", "-jar", "/home/java-app/lib/app.jar"]

EXPOSE 8080
