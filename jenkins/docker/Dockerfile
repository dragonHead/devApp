FROM jenkins/jenkins:lts

LABEL vuelearn.version="1.0"
LABEL vuelearn.description="jenkins sample"

USER root
RUN apt-get update \
  && apt-get install -y --no-install-recommends locales locales-all vim tmux \
  && apt-get clean

RUN localedef -i ja_JP -c -f UTF-8 -A /usr/share/locale/locale.alias ja_JP.UTF-8
ENV LC_ALL ja_JP.UTF-8
ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja

RUN ln -sf /usr/share/zoneinfo/Asia/Tokyo /etc/localtime

#COPY plugins.txt /usr/share/jenkins/plugins.txt
#RUN /usr/local/bin/plugins.sh /usr/share/jenkins/plugins.txt

USER jenkins
