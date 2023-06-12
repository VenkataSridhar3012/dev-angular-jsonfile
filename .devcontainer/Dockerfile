# Use the official Node.js 16 image as the base image
FROM node:16

# Set the working directory in the container
WORKDIR /workspace

# Copy the package.json and package-lock.json files to the container
COPY package*.json ./

# Install project dependencies
RUN npm install
RUN npm install -g @angular/cli

# Copy the entire project to the container
COPY . .

# Expose port 4200
EXPOSE 4200

# Start the Angular server
CMD ["ng", "serve", "--host", "0.0.0.0"]
