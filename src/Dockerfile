FROM node
RUN apt-get update -qq && apt-get install -y build-essential libpq-dev libkrb5-dev
RUN mkdir /myapp
WORKDIR /myapp
ADD package.json /myapp/package.json
RUN npm install
ADD . /myapp
EXPOSE 8080
CMD ["npm", "start"]
