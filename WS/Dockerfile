FROM centos/systemd

MAINTAINER  "Yavor Tomov" yavoritomov@gamil.com

RUN yum update -y && yum install -y httpd openssh-server openssh-clients passwd && yum clean all && systemctl enable httpd.service

RUN ( sleep .1 ; printf "%s\n" "password" "password" ) | passwd


EXPOSE 80 22

CMD ["/usr/sbin/init"]