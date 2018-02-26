FROM nginx:1.13

LABEL AUTHOR="xwzhou@yeah.net"

ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

COPY conf/nginx.conf /etc/nginx/nginx.conf

EXPOSE 80
