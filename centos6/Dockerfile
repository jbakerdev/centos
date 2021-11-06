FROM centos:6
LABEL name="jbakerdev/centos6" \
      description="jbakerdev CentOS 6"

# Update and install packages
RUN sed -i \
        -e 's|mirrorlist|#mirrorlist|g' \
        -e 's|#baseurl|baseurl|g' \
        -e 's|http://mirror.centos.org/centos/$releasever|https://vault.centos.org/6.10|g' \
        /etc/yum.repos.d/CentOS-Base.repo \
    && yum update -y \
    && yum install -y --setopt=tsflags=nodocs \
        curl \
        gcc \
        gcc-c++ \
        make \
    && yum clean all

# Set default command
CMD ["/usr/bin/bash"]
