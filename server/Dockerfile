FROM node:11.13.0
LABEL name="server"

RUN mkdir app
WORKDIR /app

COPY ./package.json /app/package.json

RUN npm install

ARG env
ARG mysqlHost
ARG mysqlPassword
ENV APP_ENV=$env
ENV MYSQL_HOST=$mysqlHost
ENV MYSQL_PASSWORD=$mysqlPassword

COPY . /app

EXPOSE 80

RUN echo 'Build Completed'

CMD ["npm","start"]
