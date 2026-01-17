# Stage 1: Build React app with Vite
FROM node:20-alpine AS build

# Set working directory
WORKDIR /app

# Copy package.json and package-lock.json (if exists)
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the project
COPY . .

# Accept build arg for backend URL
ARG VITE_BACKEND_URL
# Make it available during npm run build
ENV VITE_BACKEND_URL=$VITE_BACKEND_URL

# Build the production files
RUN npm run build

# Stage 2: Serve with Nginx
FROM nginx:alpine

# Copy built files from Stage 1
COPY --from=build /app/dist /usr/share/nginx/html

# Optional: use build argument for nginx.conf
ARG NGINX_CONF=nginx.conf
COPY ${NGINX_CONF} /etc/nginx/conf.d/default.conf

# Expose port 80
EXPOSE 80

# Start Nginx
CMD ["nginx", "-g", "daemon off;"]
