FROM kalilinux/kali-rolling

RUN pacman -Syu --noconfirm libaio pixman socat python-pyserial

WORKDIR /chall
CMD ["./run_debug.sh"]
EXPOSE 1337
