
FROM node:18-alpine
 
# Set working directory

WORKDIR /usr/src/app
 
# Copy package.json and package-lock.json from the strapi-project directory

COPY package*.json package-lock.json ./
 
# Install dependencies

RUN npm install
 
# Copy the rest of the application code into the container

COPY . .
 
# Build the Strapi project

RUN npm run build
 
# Expose the port Strapi will run on

EXPOSE 1337
 
# Start Strapi

CMD ["npm", "start"]

 
