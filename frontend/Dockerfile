FROM node:18-alpine

# Set working directory
WORKDIR /app

# Install dependencies
COPY package.json ./
RUN npm install

# Copy project files
COPY . .

# Expose dev server port
EXPOSE 5173

# Default command (overridden by docker-compose)
CMD ["npm", "run", "dev"]
