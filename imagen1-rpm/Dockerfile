FROM almalinux:9
RUN dnf -y update && \
    dnf -y install rpm-build rpmdevtools createrepo dnf-utils && \
    dnf clean all

WORKDIR /workspace
CMD ["/bin/bash"]
