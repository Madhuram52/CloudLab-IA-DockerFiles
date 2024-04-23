FROM node:18
WORKDIR /app

COPY package.json /app/package.json
COPY package-lock.json /app/package-lock.json

RUN npm install

# Copy the controllers folder
COPY controllers /app/controllers

# Copy the middleware folder
COPY middleware /app/middleware

# Copy the models folder
COPY models /app/models

# Copy the routes folder
COPY routes /app/routes

# Copy other necessary files
COPY config.js /app/
COPY server.js /app/
COPY seed.js /app/

# Expose port 5000
EXPOSE 5000

ENTRYPOINT ["npm", "start"]
