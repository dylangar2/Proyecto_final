FROM almalinux:9
RUN dnf -y update && \
    dnf -y install rpm-build rpmdevtools createrepo dnf-utils && \
    dnf clean all

WORKDIR /workspace
CMD ["/bin/bash"]

FROM almalinux:8
RUN dnf -y update &&     dnf -y install ruby ruby-devel gcc make &&     dnf clean all
RUN dnf -y install git &&     git clone https://github.com/rbenv/rbenv.git ~/.rbenv
WORKDIR /workspace
CMD ["ruby", "--version"]

FROM almalinux:8
RUN dnf module install -y nodejs:16
RUN curl -fsSL https://rpm.nodesource.com/setup_22.x | bash - &&     dnf install -y nodejs &&     dnf clean all
RUN npm install -g yarn
WORKDIR /workspace
CMD ["node", "--version"]


FROM almalinux:8
RUN dnf -y update &&     dnf -y install python3 python3-pip python3-virtualenv python3-setuptools &&     dnf clean all
WORKDIR /workspace
CMD ["python3", "--version"]
