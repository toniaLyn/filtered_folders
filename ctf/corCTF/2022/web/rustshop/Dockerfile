FROM kalilinux/kali-rolling

WORKDIR /app

COPY ./server .

RUN cargo build --release

CMD ["./target/release/rustshop"]
