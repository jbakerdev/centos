FROM ghcr.io/jbakerdev/centos7
LABEL name="jbakerdev/centos7-perl" \
      description="Arctos CentOS 7 with Perl"

# Update and install packages
RUN yum update -y \
    && yum install -y --setopt=tsflags=nodocs \
        perl-App-cpanminus \
    && yum clean all

# Install cpm/carton
RUN cpanm -nq App::cpm Carton::Snapshot

# Set default command
CMD ["/usr/bin/bash"]
