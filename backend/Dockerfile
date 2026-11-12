# Backend Dockerfile

FROM node:18-alpine
WORKDIR /usr/src/app

# Install dependencies
COPY package*.json ./
RUN npm ci --only=production

# Copy source
COPY src ./src
COPY uploads ./uploads

EXPOSE 5000

ENV NODE_ENV=production
ENV PORT=5000
CMD ["node", "src/server.js"]
