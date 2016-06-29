FROM centos
MAINTAINER shiwei-tomcat8

ADD jdk-8u91-linux-x64.tar.gz /tmp
RUN mv /tmp/jdk1.8.0_91/ /usr/lib/java/
ENV JAVA_HOME /usr/lib/java/

ADD apache-tomcat-8.0.36.tar.gz /tmp
RUN mv /tmp/apache-tomcat-8.0.36/ /opt/tomcat8/
ENV CATALINA_HOME /opt/tomcat8/
ENV PATH $PATH:$JAVA_HOME/bin:$CATALINA_HOME/bin

EXPOSE 8080

CMD /opt/tomcat8/bin/startup.sh && tail -f /opt/tomcat8/logs/catalina.out 
