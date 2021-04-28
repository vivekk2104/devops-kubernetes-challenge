FROM node:10.23.0
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app
COPY package.json ./
RUN npm install
ADD . ./
EXPOSE 3000
CMD [ "npm", "start" ]
