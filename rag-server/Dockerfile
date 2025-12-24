FROM node:20-slim

WORKDIR /app

COPY package*.json ./
RUN npm ci --only=production

COPY dist/ ./dist/
COPY data/ ./data/
COPY sources.jsonl ./

ENV PORT=8090

EXPOSE 8090

CMD ["node", "dist/index.js"]
