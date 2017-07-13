FROM node:8
MAINTAINER Dainis Lapins <dainis186@gmail.com>

WORKDIR /var/redis_commander

RUN npm install redis-commander
RUN echo '{}' > /root/.redis-commander

ENTRYPOINT ["./node_modules/.bin/redis-commander"]
