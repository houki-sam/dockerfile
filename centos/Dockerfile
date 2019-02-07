FROM centos:7

MAINTAINER YUKI HORITA <y-horita-42t@eagle.sophia.ac.jp>

RUN set -x && \
    #まずupdate&upgrade
    yum -y update && \
    yum -y upgrade && \
    yum -y install make &&\

    #postgresql関連
    yum install -y postgresql && \

    #vim関連
    yum install -y vim && \

    #セキュリテイ関連
    yum install -y sudo  &&\

    #ruby関連
    yum install -y ruby &&\
    git clone https://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build &&\
    echo '# rbenv' >> ~/.bash_profile &&\
    echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bash_profile &&\
    echo 'eval "$(rbenv init -)"' >> ~/.bash_profile &&\
    exec $SHELL --login &&\
    yum -y install bzip2 gcc openssl-devel readline-devel zlib-devel &&\
    rbenv install 2.4.5 &&\
    gem install rails bundle &&\
    
    #python関連
    yum install -y https://centos7.iuscommunity.org/ius-release.rpm &&\
    yum search -y python36 &&\
    yum install -y python36u python36u-libs python36u-devel python36u-pip &&\
    pip3.6 install --upgrade pip &&\
    pip3.6 install pandas &&\
    pip3.6 install numpy &&\
    echo '#python関連' &&\
    echo 'alias python=/usr/bin/python3.6' &&\
    echo 'alias python=/usr/bin/pip3.6' &&\

    #git関連
    yum install -y git &&\



WORKDIR /usr/src/rails

VOLUME /usr/src/rails

RUN echo



