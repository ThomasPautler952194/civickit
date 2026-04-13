FROM node:22-alpine

WORKDIR /app

# Copy package files (already inside backend context)
COPY package*.json ./

RUN npm ci

# Copy everything from backend
COPY . .

RUN npx prisma generate

EXPOSE 3000

CMD ["npm", "start"]