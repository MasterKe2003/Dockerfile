FROM openjdk:8

# 设置工作目录
WORKDIR /app

# 安装 Nginx
RUN apt-get update && \
    apt-get install -y nginx && \
    rm -rf /var/lib/apt/lists/*

# 暴露 Nginx 默认端口
EXPOSE 80