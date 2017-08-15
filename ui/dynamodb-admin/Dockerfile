FROM node:8
MAINTAINER Dainis Lapins <dainis186@gmail.com>
WORKDIR /var/
RUN echo '{ "allow_root": true }' > /root/.bowerrc
RUN npm install bower -g
RUN npm install dynamodb-admin
CMD ["./node_modules/.bin/dynamodb-admin"]
