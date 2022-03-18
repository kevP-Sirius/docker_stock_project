FROM node:16.14
## for apt to be noninteractive
ENV DEBIAN_FRONTEND noninteractive 
RUN apt install git  -y
RUN mkdir -p /var/src/app/
WORKDIR /var/src/app/
ARG CACHEBUST=0
RUN git clone https://github.com/kevP-Sirius/back-stock-projet.git
WORKDIR /var/src/app/back-stock-projet/
RUN rm -rf node_modules/
RUN npm install
RUN npm install pm2 -g
EXPOSE 9001
CMD ["node","/var/src/app/back-stock-projet/server.js"]





