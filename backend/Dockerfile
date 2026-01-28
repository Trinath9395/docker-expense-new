FROM node:20

WORKDIR /opt/backend

COPY package.json .
COPY *.js .

RUN npm install

# Non-sensitive config can stay here
ENV DB_HOST=mysql

# Fix typo: run index.js
CMD ["node", "index.js"]
