FROM redmine:4.1-passenger

RUN apt-get update \
  && apt-get install -y --no-install-recommends vim tmux curl \
  && apt-get upgrade -y \
  && apt-get clean

RUN ln -sf /usr/share/zoneinfo/Asia/Tokyo /etc/localtime

RUN curl -sSLO https://github.com/mailhog/mhsendmail/releases/download/v0.2.0/mhsendmail_linux_amd64 \
    && chmod +x mhsendmail_linux_amd64 \
    && mv mhsendmail_linux_amd64 /usr/local/bin/mhsendmail
