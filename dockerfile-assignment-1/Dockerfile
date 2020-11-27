FROM node:erbium-alpine3.10

RUN apk --version \
    apk update \
    apk add --update tini

WORKDIR /usr/src/app

COPY package.json .

RUN npm -v && node -v && npm install

RUN npm cache clean --force

COPY . .

RUN pwd && ls -al

EXPOSE 3000

CMD ["bash"]

# 11:20 11-27-2020 Assignment 1 but the CMD not working properly ??