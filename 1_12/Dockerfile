FROM ubuntu

WORKDIR /app

RUN apt-get -y update && apt-get install -y curl

RUN curl -sL https://deb.nodesource.com/setup_16.x | bash
RUN apt-get install -y nodejs

COPY . .

RUN npm install && npm run build
RUN npm install -g serve

CMD ["serve", "-s", "-l", "5001", "build"]