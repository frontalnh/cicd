FROM node:11.13.0
LABEL name="server"

RUN mkdir app
WORKDIR /app

COPY ./package.json /app/package.json

RUN npm install

ARG env
ARG mysqlHost
ENV APP_ENV=$env
ENV MYSQL_HOST=$mysqlHost

COPY . /app

EXPOSE 80

RUN echo 'Build Completed'

CMD ["npm","start"]
