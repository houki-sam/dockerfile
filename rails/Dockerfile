FROM rails:latest

MAINTAINER YUKI HORITA <y-horita-42t@eagle.sophia.ac.jp>

RUN set -x && \
    apt-get -y update && \
    apt-get -y upgrade && \
    apt-get install -y postgresql && \
    gem install bootstrap && \
    apt-get install -y vim && \
    mkdir /root/.config &&\
    mkdir /root/.config/nvim &&\
    wget https://raw.githubusercontent.com/yuki-trans-am/init.vim/master/init.vim -P /root/.config/nvim
    

WORKDIR /usr/src/rails

VOLUME /usr/src/rails

RUN echo



