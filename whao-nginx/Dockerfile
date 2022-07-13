FROM centos:7

MAINTAINER whaosoft

RUN yum -y install gcc && \
	yum install -y pcre pcre-devel \
	yum install -y zlib zlib-devel \
	yum install -y openssl openssl-devel && \
	rm -rf /var/lib/yum/lists/* # 20150205

RUN curl -O http://nginx.org/download/nginx-1.20.0.tar.gz && \
	tar zxvf nginx-1.20.0.tar.gz && \
	rm -rf *.tar.gz && \
	cd nginx-1.20.0 && \
	./configure --with-stream && \
	make && make install
CMD /usr/local/nginx/sbin/nginx && tail -f /dev/null
