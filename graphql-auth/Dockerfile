
FROM node:20 as builder

WORKDIR /src


COPY package.json  ./


RUN npm install -g pnpm


RUN pnpm install  --prod


COPY . .


RUN pnpm build


RUN npm install -g pnpm
RUN pnpm install  --prod


CMD ["node"]
