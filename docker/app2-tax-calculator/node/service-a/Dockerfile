FROM node:24-slim
WORKDIR /index
COPY package*.json ./
RUN npm install --production
COPY . .
EXPOSE 3000
CMD [ "node", "index.js" ]