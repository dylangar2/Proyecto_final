FROM almalinux:8
RUN dnf -y update &&     dnf -y install python3 python3-pip python3-virtualenv python3-setuptools &&     dnf clean all
WORKDIR /workspace
CMD ["python3", "--version"]
