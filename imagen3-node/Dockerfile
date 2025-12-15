FROM almalinux:8

RUN dnf module reset nodejs -y \
 && dnf module enable nodejs:16 -y \
 && dnf install -y nodejs npm \
 && dnf clean all

RUN npm install -g yarn

WORKDIR /workspace
