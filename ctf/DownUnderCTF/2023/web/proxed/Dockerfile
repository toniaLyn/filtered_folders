FROM kalilinux/kali-rolling

WORKDIR /app

COPY . ./

RUN go build -o app ./...

EXPOSE 8081

USER goodboy:goodboy

CMD ["./app"]
