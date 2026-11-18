FROM ubuntu:24.04

WORKDIR /usr/src/app

COPY script.sh .

RUN <<EOF
apt-get update
apt-get install -y curl
EOF

CMD ["./script.sh"]