FROM ubuntu:20.04

WORKDIR /usr/src/app

EXPOSE 5000

COPY . .
RUN apt-get update &&  apt-get install -y curl

RUN curl -sL https://deb.nodesource.com/setup_16.x | bash && apt install -y nodejs

RUN npm install 
RUN npm run build
RUN npm install -g serve

CMD ["serve", "-s", "-l", "5000", "build"]
