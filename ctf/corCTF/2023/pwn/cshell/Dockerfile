FROM kalilinux/kali-rolling
RUN apt-get update && \
    apt-get -y install libreadline-dev && \
    rm -rf /var/lib/apt/lists/*

FROM kalilinux/kali-rolling
COPY --from=run / /srv
WORKDIR /srv/app
COPY boat.exe flag.txt /srv/app/
COPY start_boats.sh /srv/app/run
ENV JAIL_MEM=1G JAIL_CPU=500 JAIL_TIME=300 JAIL_PIDS=20
