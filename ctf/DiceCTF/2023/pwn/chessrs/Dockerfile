# build phase
FROM kalilinux/kali-rolling

WORKDIR /app
COPY ./app .
RUN cargo build --release

# final image
FROM kalilinux/kali-rolling

WORKDIR /app
COPY --from=builder /app/target/release/app ./
COPY --from=builder /app/static ./static/

RUN useradd -ms /bin/bash user
USER user

CMD ["/app/app"]