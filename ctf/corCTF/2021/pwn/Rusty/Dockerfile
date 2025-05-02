FROM kalilinux/kali-rolling

ENV JAIL_TIME=600

COPY --from=ubuntu:18.04 / /srv
RUN mkdir /srv/app
COPY bin/ /srv/app
