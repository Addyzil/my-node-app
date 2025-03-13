# Use a base Node.js image
FROM mcr.microsoft.com/devcontainers/javascript-node:latest

# Install additional dependencies
RUN apt-get update && apt-get install -y \
    curl \
    vim \
    && rm -rf /var/lib/apt/lists/*

# Set working directory
WORKDIR /workspace

# Install project dependencies
COPY package.json package-lock.json ./
RUN npm install

# Expose port 3000 for the Node.js server
EXPOSE 3000

# Default command
CMD ["node"]
