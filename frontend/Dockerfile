FROM tomcat:9.0-slim
WORKDIR /opt
ENV APP_HOME=/usr/local/tomcat
ENV PORT=8080
ADD https://s3-us-west-2.amazonaws.com/studentapi-cit/student.war $APP_HOME/webapps/
ADD https://s3-us-west-2.amazonaws.com/studentapi-cit/mysql-connector.jar $APP_HOME/lib
COPY config /opt
RUN sed -i '20r /opt/config' /usr/local/tomcat/conf/context.xml
EXPOSE $PORT
CMD ["catalina.sh", "run"]
