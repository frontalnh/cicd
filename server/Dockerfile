FROM node:11.13.0
LABEL name="server"

RUN mkdir app
WORKDIR /app

COPY ./package.json /app/package.json

RUN npm install

ENV APP_ENV=prod
ENV AWS_ACCESS_KEY_ID='hello'
ENV AWS_SECRET_ACCESS_KEY='secret'

COPY . /app

EXPOSE 3001

RUN echo 'Build Completed'

CMD ["npm","start"]

