FROM node:20.18.3-alpine3.21
RUN addgroup -S expense && adduser -S expense -G expense && \
    mkdir /opt/backend && \
    chown -R expense:expense /opt/backend 
WORKDIR /opt/backend

COPY package.json .
COPY *.js .

RUN npm install

# Non-sensitive config can stay here
ENV DB_HOST="mysql"
# ENV DB_HOST="localhost"
USER expense
# Fix typo: run index.js
CMD ["node", "index.js"]
