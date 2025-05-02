FROM kalilinux/kali-rolling
WORKDIR /usr/src/app
COPY package.json .
RUN npm install
COPY . .
RUN npm run build

FROM kalilinux/kali-rolling
WORKDIR /usr/src/app
COPY api/package.json .
RUN npm install
COPY api .
RUN npm run build

FROM kalilinux/kali-rolling
WORKDIR /usr/src/app
COPY --from=frontend-build /usr/src/app/build build/
COPY --from=backend-build /usr/src/app api/
COPY flag.txt .
EXPOSE 3000
CMD [ "node", "api/dist/index.js" ]
