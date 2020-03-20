#https://hub.docker.com/r/gitbucket/gitbucket/
FROM openjdk:8-jre

LABEL vuelearn.version="1.0"
LABEL vuelearn.description="redmine sample"

RUN apt-get update \
  && apt-get install -y --no-install-recommends locales locales-all \
  && apt-get clean

RUN localedef -i ja_JP -c -f UTF-8 -A /usr/share/locale/locale.alias ja_JP.UTF-8
ENV LC_ALL ja_JP.UTF-8
ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja

RUN ln -sf /usr/share/zoneinfo/Asia/Tokyo /etc/localtime

ADD https://github.com/gitbucket/gitbucket/releases/download/4.33.0/gitbucket.war /opt/gitbucket.war
RUN ln -s /gitbucket /root/.gitbucket
VOLUME /gitbucket

# Port for web page and Port for SSH access to git repository (Optional)
EXPOSE 8080 29418

CMD ["sh", "-c", "java -jar /opt/gitbucket.war"]