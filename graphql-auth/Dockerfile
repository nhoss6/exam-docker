
FROM node:latest as builder

WORKDIR /app


COPY package.json pnpm-lock.yaml ./


RUN npm install -g pnpm


RUN pnpm install  --prod


COPY . .


RUN pnpm build

FROM node:latest

WORKDIR /app

COPY --from=builder /app/dist ./dist
COPY --from=builder /app/package.json /app/pnpm-lock.yaml ./

RUN npm install -g pnpm
RUN pnpm install  --prod

ENV NODE_ENV=production

CMD ["node", "dist/index.js"]
