# ===== build =====
FROM node:20-bullseye AS build
WORKDIR /app

ARG NEXT_PUBLIC_API_URL
ENV NEXT_PUBLIC_API_URL=$NEXT_PUBLIC_API_URL

COPY package.json package-lock.json* ./

RUN npm config set legacy-peer-deps true \
 && if [ -f package-lock.json ]; then npm ci; else npm install; fi

COPY . .

RUN npm run build

# ===== runtime =====
FROM node:20-bullseye-slim
WORKDIR /app
ENV NODE_ENV=production
COPY --from=build /app ./
EXPOSE 3000
CMD ["npm", "start"]

