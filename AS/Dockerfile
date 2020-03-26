FROM node:10

WORKDIR /usr/src/app

COPY package*.json ./
RUN npm install
# for production
# RUN npm ci --only=production

COPY . .

# Expose HTTPS and HTTP port
EXPOSE 8001
EXPOSE 3001
# allows passing of command line arguments in docker compose using command
ENTRYPOINT [ "npm", "run", "start" ]
