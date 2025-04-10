# Use Node.js official image
FROM node:16

# Set working directory inside the container
WORKDIR /app

# Install dependencies
COPY package.json package-lock.json ./
RUN npm install

# Copy the rest of the application files
COPY . .

# Expose the port your Next.js app will run on
EXPOSE 3000

# Start Next.js app
CMD ["npm", "run", "dev"]