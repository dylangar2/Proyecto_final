FROM almalinux:8
RUN dnf module install -y nodejs:16
RUN curl -fsSL https://rpm.nodesource.com/setup_22.x | bash - &&     dnf install -y nodejs &&     dnf clean all
RUN npm install -g yarn
WORKDIR /workspace
CMD ["node", "--version"]
