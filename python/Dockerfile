FROM python:3.5

MAINTAINER YUKI HORITA <y-horita-42t@eagle.sophia.ac.jp>

RUN set -x && \
    #更新
    apt-get -y update && \
    apt-get -y upgrade && \
    #最低限のパッケージ
    apt-get install -y wget &&\
    #vim関連
    apt-get install -y vim && \
    mkdir ~/.vim &&\
    mkdir ~/.vim/rc &&\
    mkdir ~/.vim/colors &&\
    #.vimrcをダウンロード
    wget https://raw.githubusercontent.com/yuki-trans-am/vim/master/.vimrc -P /root/ &&\
    wget https://raw.githubusercontent.com/yuki-trans-am/vim/master/dein.toml -P /root/.vim/rc &&\
    wget https://raw.githubusercontent.com/yuki-trans-am/vim/master/dein_lazy.toml -P /root/.vim/rc &&\
    wget https://raw.githubusercontent.com/freeo/vim-kalisi/master/colors/kalisi.vim -P /root/.vim/colors

RUN pip install pandas\
                schedule\
                numpy\
                django

WORKDIR /python





