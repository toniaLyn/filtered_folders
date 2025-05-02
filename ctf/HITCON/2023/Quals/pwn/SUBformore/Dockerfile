FROM kalilinux/kali-rolling

WORKDIR /app
COPY run.sh run
COPY lessequalmore lessequalmore
COPY chal.txt chal.txt
COPY flag.txt flag.txt


FROM kalilinux/kali-rolling
COPY --from=base / /srv
ENV JAIL_TIME=30 JAIL_CPU=500 JAIL_MEM=10M
