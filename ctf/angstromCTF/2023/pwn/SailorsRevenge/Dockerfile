FROM kalilinux/kali-rolling

ENV TINI_VERSION v0.19.0
ADD https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini /tini
RUN chmod +x /tini
ENTRYPOINT ["/tini", "--"]

RUN apt-get update -y && apt-get install -y pkg-config libudev-dev libssl-dev

COPY ./server /app
WORKDIR /app

RUN cargo build --release && cp target/release/server . && cargo clean

FROM kalilinux/kali-rolling

COPY --from=build /app/server /app/server
COPY ./flag.txt /app/flag.txt
COPY ./sailors_revenge.so /app/sailors_revenge.so
WORKDIR /app

CMD ["/app/server"]
