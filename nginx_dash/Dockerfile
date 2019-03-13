# FROM ubuntu:16.04
# ADD ./server
# WORKDIR /server
# RUN apt-get update && apt-get install -y \
#     apt-get build-dep nginx && \
#     apt-get source nginx && \
#     git clone https://github.com/ut0mt8/nginx-rtmp-module/ && \
#     cd nginx-1.10.0 \
#     ./configure --add-module=../nginx-rtmp-module && \
#     make && \
#     make install && \
#     wget https://isrv.pw/html5-live-streaming-with-mpeg-dash/nginx.service.txt -O /lib/systemd/system/nginx.service && \
#     systemctl daemon-reload && \
#     systemctl enable nginx.service && \
FROM nginx
# ADD . /server
# WORKDIR /server
# # COPY video /usr/share/nginx/html
# RUN git clone https://github.com/Dash-Industry-Forum/dash.js.git && \
#     npm install -g grunt-cli && \
#     npm install