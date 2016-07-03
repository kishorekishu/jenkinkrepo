FROM dockerfile/java:oracle-java8

ADD testmvn.jar /opt/testmvn/
EXPOSE 8080
WORKDIR /opt/testmvn/
CMD ["java", "-Xms512m", "-Xmx1g", "-jar", "testmvn.jar"]