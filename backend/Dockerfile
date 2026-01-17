# Stage 1: install production deps
FROM node:lts-alpine AS deps
WORKDIR /app
COPY package*.json ./
RUN npm ci --omit=dev

# Stage 2: runtime
FROM node:lts-alpine AS runner
WORKDIR /app
ENV NODE_ENV=production
COPY package*.json ./
COPY --from=deps /app/node_modules ./node_modules
COPY src ./src
EXPOSE 3000
CMD ["node", "src/index.js"]
