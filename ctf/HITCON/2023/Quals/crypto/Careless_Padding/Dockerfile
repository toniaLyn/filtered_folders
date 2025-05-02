FROM kalilinux/kali-rolling

WORKDIR /app
RUN pip install pycryptodome
COPY chal.py run
COPY secret.py secret.py

FROM kalilinux/kali-rolling
COPY --from=base / /srv
ENV JAIL_TIME=30 JAIL_CPU=500 JAIL_MEM=10M
