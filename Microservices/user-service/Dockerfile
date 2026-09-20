FROM node:18-alpine AS base

WORKDIR /app/user-service

COPY package*.json ./
RUN npm install --production

COPY . ./
ENV NODE_ENV=production
EXPOSE 3000

CMD ["npm", "run", "start"]
