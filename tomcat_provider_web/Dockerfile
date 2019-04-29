# Dockerfile for provider web
# VERSION 0.0.1
# Author: XiaoMi

FROM tomcat:8-jre8

MAINTAINER XiaoMi <homillyxiao@gmail.com>

#定义工作目录
ENV WORK_PATH /usr/local/tomcat/conf

#定义manager.xml工作目录
ENV MANAGER_PATH /usr/local/tomcat/conf/Catalina/localhost
 
#定义要替换的文件名
ENV USER_CONF_FILE_NAME tomcat-users.xml
 
#定义要替换的server.xml文件名
ENV SERVER_CONF_FILE_NAME server.xml
 
#定义要新增的manager.xml文件名
ENV MANAGER_CONF_FILE_NAME manager.xml
 
#删除原文件tomcat-users.xml
RUN rm $WORK_PATH/$USER_CONF_FILE_NAME
 
#复制文件tomcat-users.xml
COPY  ./$USER_CONF_FILE_NAME $WORK_PATH/
 
#删除原文件server.xml
RUN rm $WORK_PATH/$SERVER_CONF_FILE_NAME
 
#复制文件server.xml
COPY  ./$SERVER_CONF_FILE_NAME $WORK_PATH/
 
#复制文件manager.xml
COPY  ./$MANAGER_CONF_FILE_NAME $MANAGER_PATH/
