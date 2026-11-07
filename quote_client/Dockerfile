FROM node:19.5.0-buster-slim@sha256:871673a1451a2d0a8b0e2a08d1d89a5f6f3b91d158eae8d4d3aa7f77bb7b5c3f 

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
