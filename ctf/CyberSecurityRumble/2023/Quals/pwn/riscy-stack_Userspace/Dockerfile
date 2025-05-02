FROM kalilinux/kali-rolling

RUN apt-get update && apt-get install -y --no-install-recommends socat qemu-system-riscv64
RUN useradd -UM chall

COPY . /app

WORKDIR /app

CMD /app/socat.sh
