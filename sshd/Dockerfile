FROM centos
MAINTAINER huzichun
RUN yum -y install openssh-server
RUN echo "root:123456" | chpasswd
RUN ssh-keygen -t rsa -f /etc/ssh/ssh_host_rsa_key
RUN ssh-keygen -t dsa -f /etc/ssh/ssh_host_ecdsa_key
RUN sed -i 's/UsePAM yes/#UsePAM yes/g' /etc/ssh/sshd_config
EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]
