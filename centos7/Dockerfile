FROM centos:7
LABEL name="jbakerdev/centos7" \
      description="jbakerdev CentOS 7"

# Update and install packages
RUN yum update -y \
    && yum install -y --setopt=tsflags=nodocs \
        curl \
        gcc \
        gcc-c++ \
        git \
        make \
    && yum clean all

# Set default command
CMD ["/usr/bin/bash"]
