FROM node:18
WORKDIR /app

COPY package.json /app/package.json
COPY package-lock.json /app/package-lock.json

RUN npm install

# Copy the source code and other necessary files
COPY src /app/src
COPY public /app/public
COPY index.html /app/
COPY README.md /app/
COPY vite.config.js /app/

# Expose port 5173
EXPOSE 5173

# Command to start the application
ENTRYPOINT ["npm", "run", "dev"]
