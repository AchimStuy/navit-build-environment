FROM debian:stable

RUN apt update \
    && apt install -y --no-install-recommends wget \
    && apt clean \
    && apt autoremove

RUN wget -c https://master.dl.sourceforge.net/project/cegcc/cegcc/0.59.1/mingw32ce-0.59.1.tar.bz2 \
    -O mingw32ce-0.59.1.tar.bz2 --no-check-certificate && tar xvjpf mingw32ce-0.59.1.tar.bz2 \
    && rm mingw32ce-0.59.1.tar.bz2

ENV MINGW32CE_PATH="/opt/mingw32ce"
ENV PATH=$PATH:$MINGW32CE_PATH/bin