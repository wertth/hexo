# 使用官方 Node.js 镜像作为基础镜像
FROM node:16

# 设置工作目录
WORKDIR /workspace

# 安装 Hexo CLI
RUN npm install -g hexo-cli && hexo -v

# 安装 Python 和 Jupyter Notebook
RUN apt-get update && apt-get install -y python3 python3-pip && \
    pip3 install --upgrade pip && \
    pip3 install jupyter && pip3 install notebook

# 暴露 Hexo 默认端口
EXPOSE 4000

# 暴露 Jupyter Notebook 默认端口
EXPOSE 8888

# 设置命令启动时的入口点
CMD ["bash"]
