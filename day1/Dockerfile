# Use official Node.js LTS image
FROM node:18-alpine

# Set working directory
WORKDIR /day1
# Copy dependency definitions
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the app code
COPY . .

# Expose the app port
EXPOSE 8080

# Start the app
CMD ["npm", "start"]
