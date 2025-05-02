FROM kalilinux/kali-rolling

WORKDIR /app
COPY package.json .
RUN npm i

COPY box.html web.js ./

USER node
CMD node web.js