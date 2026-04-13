FROM node:20-alpine

WORKDIR /app

# Copy package files
COPY backend/package*.json ./

# Install production dependencies
RUN npm ci --only=production

# Copy source code
COPY backend/ ./

# Generate Prisma Client
RUN npx prisma generate

EXPOSE 3000

# Change this if your package.json start script is different
CMD ["npm", "start"]