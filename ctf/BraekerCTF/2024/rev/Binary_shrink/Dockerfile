FROM kalilinux/kali-rolling

RUN useradd -m ctf
WORKDIR /home/ctf

COPY ./binary_shrink .

ENTRYPOINT ./binary_shrink