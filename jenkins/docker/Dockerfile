FROM jenkins/jenkins:lts

USER root
RUN apt-get update \
  && apt-get install -y --no-install-recommends vim tmux \
  && apt-get clean

#COPY plugins.txt /usr/share/jenkins/plugins.txt
#RUN /usr/local/bin/plugins.sh /usr/share/jenkins/plugins.txt

USER jenkins
