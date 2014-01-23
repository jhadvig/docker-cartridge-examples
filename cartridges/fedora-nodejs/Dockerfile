FROM goldmann/f20

RUN yum install -y nodejs npm

RUN mkdir -p /opt/openshift

RUN groupadd -r nodejs_app -g 433 && \
	useradd -u 431 -r -g nodejs_app -d /opt/openshift -s /sbin/nologin -c "nodejs cartridge user" nodejs_app

ADD ./prepare /opt/openshift/prepare
ADD ./start /opt/openshift/launch

RUN chown nodejs_app /opt/openshift