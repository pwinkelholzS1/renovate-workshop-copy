FROM node:20.15.0-buster-slim@sha256:b5c14e85662c43b8c86a3a88259a34f0071474ad0a029ecb4ec39bbea588b030 

WORKDIR /app
COPY package.json ./
COPY tsconfig.json ./
COPY tsconfig.node.json ./
COPY postcss.config.cjs ./
COPY tailwind.config.cjs ./
COPY vite.config.ts ./
COPY public/ ./public
COPY index.html ./

COPY src/ ./src
RUN npm install -g typescript
RUN npm install
RUN npm run build
EXPOSE 5173

ENTRYPOINT [ "npm", "run", "dev", "--host"]
