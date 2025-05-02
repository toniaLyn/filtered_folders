FROM kalilinux/kali-rolling
WORKDIR /app
COPY ./server/package.json ./server/package-lock.json ./
RUN --mount=type=cache,target=/root/.npm npm ci
COPY ./server .
CMD ["node", "index.js"]
