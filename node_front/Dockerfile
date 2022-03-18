FROM node:16.14
RUN apt install git
RUN mkdir -p /var/www/html
WORKDIR /var/www/html
ARG CACHEBUST=0
RUN git init
RUN git pull https://github.com/kevP-Sirius/front-stock-projet.git
RUN npm install -g serve
RUN npm install
RUN npm run build --prod
CMD ["serve","-s","/var/www/html/build/"]







