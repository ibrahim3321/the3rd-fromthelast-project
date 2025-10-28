FROM node:20-bullseye AS builder

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

RUN npm run build


FROM node:20-bullseye
WORKDIR /app

COPY --from=builder /app/dist ./dist
COPY package*.json ./

RUN npm install --omit=dev

EXPOSE 8706

ENV NODE_ENV=production

CMD ["npm", "start"]
