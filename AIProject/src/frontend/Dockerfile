# WorldForge/src/frontend/Dockerfile

FROM node:18-slim

# Set working directory
WORKDIR /app

# Copy package.json and install dependencies
COPY package.json package-lock.json ./
RUN npm install

# Copy all project files
COPY . .

# Build the project
RUN npm run build

# Install a simple HTTP server to serve static files
RUN npm install -g http-server

# Expose port
EXPOSE 8080

# Serve the built static files
CMD ["http-server", "dist", "-p", "8080"]
