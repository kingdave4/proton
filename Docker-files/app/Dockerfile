FROM maven:3.9.9-eclipse-temurin-21-jammy AS BUILT_IMAGE
LABEL "PROJECT"="Vprofile-v2"
LABEL  "Author"="Kingdave"
RUN git clone https://github.com/kingdave4/proton.git
RUN cd proton && git checkout containers && mvn install


FROM tomcat:10-jdk21
LABEL "PROJECT"="Vprofile-v2"
LABEL  "Author"="Kingdave"
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=BUILT_IMAGE /proton/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war


EXPOSE 8080
CMD ["catalina.sh", "run"]
