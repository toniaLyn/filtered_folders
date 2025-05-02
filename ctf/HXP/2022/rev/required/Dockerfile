# see docker-compose.yml

FROM kalilinux/kali-rolling

RUN useradd --create-home --shell /bin/bash ctf
WORKDIR /home/ctf

COPY flag files/* /home/ctf/

USER ctf

CMD sh run.sh