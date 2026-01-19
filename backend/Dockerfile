FROM node:20-alpine

WORKDIR /app

COPY package.json ./
RUN npm install --no-fund --no-audit

COPY prisma ./prisma
COPY src ./src

EXPOSE 3000
CMD ["npm", "run", "start"]
