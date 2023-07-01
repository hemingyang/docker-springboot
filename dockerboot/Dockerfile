##下载openjdk docker hub
FROM openjdk:17
##LABEL 为镜像添加元数据
LABEL authors="hemingyang"
##ARG 构建参数 格式：ARG <参数名>[=<默认值>]
ARG JAR_FILE=target/*.jar
##COPY 复制文件  COPY [--chown=<user>:<group>] <源路径>... <目标路径>
##COPY 复制文件  COPY [--chown=<user>:<group>] ["<源路径1>",... "<目标路径>"]
COPY ./target/dockerboot-0.0.1-SNAPSHOT.jar app.jar
##ENTRYPOINT 入口点  <ENTRYPOINT> "<CMD>"
ENTRYPOINT ["java", "-jar","/app.jar"]
##WORKDIR 指定工作目录
##  WORKDIR /app
##ADD 更高级的复制文件
## ADD --chown=55:mygroup files* /mydir/
##ENV 设置环境变量
## ENV VERSION=1.0 DEBUG=on \
##    NAME="Happy Feet"