# Use an official Node.js runtime as a parent image
FROM node:14

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy the current directory contents into the container
COPY . .

# Install dependencies
RUN npm install

# Make the app available on port 3000
EXPOSE 3000

# Define the command to run the app
CMD ["node", "server.js"]
