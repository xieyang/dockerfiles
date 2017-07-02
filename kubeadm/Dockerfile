FROM centos:7.2.1511
MAINTAINER pigyang <372282766.qq.com>

ADD init.sh /init.sh

RUN chmod a+x /init.sh \
    && ./init.sh \
    && rm -rf /init.sh \
    && mkdir -p /xy \
    && yum clean all \
    && yum makecache \
    && yum install --downloadonly --downloaddir=/xy kubelet kubeadm -y
