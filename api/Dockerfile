# SpotESIfy API - Dockerfile 
FROM node:20-alpine

WORKDIR /app

COPY . .

RUN apk add --no-cache curl && npm install

EXPOSE 5000

USER node

HEALTHCHECK --interval=10s --timeout=3s --retries=3 \
  CMD curl -f http://localhost:5000/api/health || exit 1

CMD ["npm", "start"]
