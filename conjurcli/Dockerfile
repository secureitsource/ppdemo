FROM centos:7
RUN yum -y install systemd openssh openssh-clients openssh-server iproute net-tools dmidecode tar which pciutils rsyslog tar sudo vim wget curl crontabs; \
    yum upgrade -y && \
    yum clean all;
RUN echo 'root:Cyberark1' | chpasswd
VOLUME [ “/sys/fs/cgroup” ]
ENTRYPOINT ["/usr/sbin/init"]
RUN wget https://github.com/cyberark/conjur-cli/releases/download/v5.4.0/conjur-5.4.0-1.el6.x86_64.rpm
RUN yum -y install conjur-5.4.0-1.el6.x86_64.rpm
