FROM nginx:1.14.2-alpine
WORKDIR /usr/share/nginx/html
RUN apk add git nodejs nodejs-npm
RUN git clone https://github.com/Dash-Industry-Forum/dash.js.git && \  
    cd dash.js && \
    npm install && \
    npm install grunt-cli && \
    npm run-script build