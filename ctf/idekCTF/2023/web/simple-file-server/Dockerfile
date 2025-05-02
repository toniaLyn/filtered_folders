FROM kalilinux/kali-rolling

RUN apt update && apt install -y \
        sqlite3 zip unzip \
    && rm -rf /var/lib/apt/lists/*

# pip
RUN pip install --no-cache-dir flask gunicorn

COPY src/ /app
WORKDIR /app

RUN chmod 4755 flag
RUN chmod 600 flag.txt

CMD bash -c "mkdir /tmp/uploadraw /tmp/uploads && sqlite3 /tmp/database.db \"CREATE TABLE users(username text, password text, admin boolean)\" && /usr/local/bin/gunicorn --bind 0.0.0.0:1337 --config config.py --log-file /tmp/server.log wsgi:app"
