FROM tomcat:9.0-slim
WORKDIR /opt
ENV APP_HOME=/usr/local/tomcat
ADD https://github.com/mayur4279/tmp/raw/main/student.war $APP_HOME/webapps/
ADD  https://github.com/mayur4279/tmp/raw/main/mysql-connector.jar $APP_HOME/lib
COPY config /opt
RUN sed -i '20r /opt/config' /usr/local/tomcat/conf/context.xml
EXPOSE 8080
CMD ["catalina.sh", "run"]
