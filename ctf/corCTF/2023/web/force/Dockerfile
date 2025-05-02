FROM kalilinux/kali-rolling

WORKDIR /app
COPY src/package* .
RUN npm ci

COPY src/ .

CMD ["node", "--expose-gc", "web.js"]