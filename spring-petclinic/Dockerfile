# take amazon correto 17 as a base image
FROM amazoncorretto:17
# add metadata
LABEL author="anitha"
LABEL project="learning"
#creating folder and adding permissions
#RUN mkdir /spc && chown nobody /spc
#creating user
USER nobody
#change the current directory
#WORKDIR /spc
# Download_url with a default value
ARG DOWNLOAD_URL="https://khajareferenceapps.s3.ap-south-1.amazonaws.com/spring-petclinic-3.2.0-SNAPSHOT.jar"
# download spring petclinic
RUN curl -O ${DOWNLOAD_URL}
# expose 8080 port as spring petclinic needs 8080
EXPOSE 8080
# command to start the application
CMD ["java", "-jar", "spring-petclinic-3.2.0-SNAPSHOT.jar"]
