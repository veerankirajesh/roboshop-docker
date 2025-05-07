
FROM node:18
EXPOSE 8080
WORKDIR /opt/server
ENV MONGO=true
COPY package.json /opt/server/
COPY server.js /app/server.js
RUN npm install
CMD ["node", "server.js"]