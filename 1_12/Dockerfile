FROM ubuntu

EXPOSE 5001

WORKDIR /usr/src/app

COPY package.json package-lock.json ./

RUN <<EOF
apt-get update
apt-get install -y curl
EOF

RUN <<EOF
curl -sL https://deb.nodesource.com/setup_16.x | bash
apt-get install -y nodejs
npm install
EOF

COPY . .

RUN REACT_APP_BACKEND_URL=http://localhost:5001 npm run build

RUN npm install -g serve

CMD ["serve", "-s", "-l", "5001", "build"]