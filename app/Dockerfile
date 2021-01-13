FROM node as APP
WORKDIR /usr/src/app
COPY . .
RUN npm install

FROM node:alpine
COPY --from=app /usr/src/app /usr/src/app
WORKDIR /usr/src/app
EXPOSE 3000
CMD ["node", "app.js"]
