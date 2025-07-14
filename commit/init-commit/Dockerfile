FROM alpine:3.18

# 安装 git 和 bash
RUN apk add --no-cache git bash

# 创建工作目录
RUN mkdir -p /challenge/level1

# 设置工作目录
WORKDIR /challenge/level1

# 添加 flag
RUN echo "FLAG{example_flag_level1}" > /flag \
    && chmod 444 /flag

# 复制关卡文件
COPY DESCRIPTION.md /challenge/level1/DESCRIPTION.md
COPY check /challenge/level1/check
COPY init /challenge/level1/init

RUN chmod +x /challenge/level1/check \
    && chmod +x /challenge/level1/init

# 删除 mkdir/rm/mv/cp 等命令防止作弊
RUN rm -f /bin/mkdir /bin/rm /bin/mv /bin/cp

# 进入容器时运行 init 脚本
CMD ["/bin/bash","/challenge/level1/init"]
