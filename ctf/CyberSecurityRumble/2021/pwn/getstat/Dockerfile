FROM kalilinux/kali-rolling

COPY . /app

WORKDIR /app

RUN apt-get update && apt-get install -y socat
RUN useradd -UM chall

CMD /app/start.sh
