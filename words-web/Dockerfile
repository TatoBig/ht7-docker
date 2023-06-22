FROM node:16

WORKDIR /app

COPY package*.json ./
COPY prisma ./prisma/
COPY .env ./
COPY tsconfig.json ./
COPY . .

RUN npm install
RUN npm run build

RUN npx prisma generate

EXPOSE 3001
CMD npm run preview