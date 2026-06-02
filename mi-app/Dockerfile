FROM node:25-alpine3.22

WORKDIR /mi-app


COPY . .


RUN yarn install --production
EXPOSE 3000


CMD ["node", "/mi-app/src/index.js"]
