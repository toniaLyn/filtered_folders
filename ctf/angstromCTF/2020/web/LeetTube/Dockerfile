FROM kalilinux/kali-rolling
COPY app /app
RUN useradd -ms /bin/bash app
RUN chown -R app /app
USER app
EXPOSE 8000
ENTRYPOINT cd /app && ./leettube.py
