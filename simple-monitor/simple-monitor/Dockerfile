# workaround for https://github.com/zeebe-io/zeebe-simple-monitor/issues/104
FROM camunda/zeebe-simple-monitor:0.17.0-alpha1 as source

FROM openjdk:11-jre

EXPOSE 8080

COPY --from=source /usr/local/zeebe-simple-monitor.jar /usr/local/zeebe-simple-monitor.jar

ENTRYPOINT ["java", "-jar", "/usr/local/zeebe-simple-monitor.jar"]
