FROM node:17
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm install
COPY . .
LABEL "s5carles"
EXPOSE 3000
ENTRYPOINT ["node"]
CMD [ "app.js" ]
