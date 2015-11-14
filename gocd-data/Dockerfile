FROM busybox

COPY conf/cruise-config.xml /etc/go/cruise-config.xml
COPY home/ssh /var/go/.ssh
RUN	chmod 600 /var/go/.ssh/id_dsa
RUN chmod 700 /var/go/.ssh
COPY home/ssh /root/.ssh
RUN	chmod 600 /root/.ssh/id_dsa
RUN chmod 700 /root/.ssh
COPY home/docker /root/.docker
COPY home/tutum/tutum /root/.tutum
COPY home/maven-settings.xml /root/.m2/


RUN chown -R 999:999 /etc/go /var/go

CMD tail -f /etc/go/cruise-config.xml
VOLUME ["/etc/go/"]
VOLUME ["/var/go/.ssh"]
VOLUME ["/root/"]
