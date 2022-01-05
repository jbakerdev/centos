FROM centos:8
LABEL name="jbakerdev/centos8" \
      description="jbakerdev CentOS 8"

# Update and install packages
RUN dnf update -y \
    && dnf install -y --setopt=tsflags=nodocs \
        curl \
        gcc \
        gcc-c++ \
        git \
        make \
    && dnf clean all

# Set default command
CMD ["/usr/bin/bash"]
