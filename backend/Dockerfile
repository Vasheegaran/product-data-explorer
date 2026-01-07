FROM apify/actor-node-playwright-chrome:latest

USER root

WORKDIR /app

COPY package*.json ./

# IMPORTANT: install devDependencies also
RUN npm install --include=dev

COPY . .

RUN npm run build

EXPOSE 3000

CMD ["npm", "run", "start:prod"]
