FROM almalinux:8
RUN dnf -y update &&     dnf -y install ruby ruby-devel gcc make &&     dnf clean all
RUN dnf -y install git &&     git clone https://github.com/rbenv/rbenv.git ~/.rbenv
WORKDIR /workspace
CMD ["ruby", "--version"]
