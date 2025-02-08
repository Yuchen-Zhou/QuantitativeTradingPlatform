# 使用官方 Python 3.11 镜像作为基础镜像
FROM python:3.11-slim

# 设置环境变量，确保 Python 输出不缓冲
ENV PYTHONUNBUFFERED=1

# 创建并设置工作目录
WORKDIR /workspace

RUN apt-get update && \
    apt-get install -y libpq-dev gcc build-essential

# 安装项目依赖
COPY ./requirements.txt /workspace/requirements.txt
RUN pip install --upgrade pip
RUN pip install -r requirements.txt

# 暴露端口 8000
EXPOSE 8000
