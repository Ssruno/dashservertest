FROM nginx:1.14.2-alpine
# ADD . /server
WORKDIR /usr/share/nginx/html
# WORKDIR /server
# RUN apt-get update && \
    # apt-get upgrade -y && \
    # apt-get install -y git && \
# RUN npm install -g grunt-cli
RUN apk add git nodejs nodejs-npm
RUN git clone https://github.com/Dash-Industry-Forum/dash.js.git && \
    # npm install -g grunt-cli && \
    cd dash.js && \
    npm install && \
    npm install grunt-cli 
    
    # grunt dev