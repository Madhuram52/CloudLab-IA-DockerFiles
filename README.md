# CloudLab-IA-DockerFiles

<h1>Frontend-Dockerfile :</h1>

<h5>FROM node:18:</h5> Specifies the base image as Node.js version 18.

<h5>WORKDIR /app:</h5> Sets the working directory inside the container to /app.

<h5>COPY package.json /app/package.json and COPY package-lock.json /app/package-lock.json:</h5> Copies Node.js project configuration files.

<h5>RUN npm install:</h5> Installs project dependencies.

<h5>COPY src /app/src, COPY public /app/public, COPY index.html /app/, COPY README.md /app/, COPY vite.config.js /app/:</h5> Copies project source code and configuration files.

<h5>EXPOSE 5173:</h5> Exposes port 5173 for external connections.

<h5>ENTRYPOINT ["npm", "run", "dev"]:</h5> Sets the command to start the application as npm run dev.


<h1>Backend-DockerFile : </h1>

<h5>FROM node:18:</h5> Specifies the base image as Node.js version 18.

<h5>WORKDIR /app:</h5> Sets the working directory inside the container to /app. All subsequent commands will be executed relative to this directory.

<h5>COPY package.json /app/package.json and COPY package-lock.json /app/package-lock.json:</h5> Copies Node.js project configuration files.

<h5>RUN npm install:</h5> Installs project dependencies based on the package.json and package-lock.json files.

<h5>COPY controllers /app/controllers, COPY middleware /app/middleware, COPY models /app/models, COPY routes /app/routes:</h5> Copies various directories (controllers, middleware, models, routes) from the host machine to corresponding directories inside the container's /app directory. These likely contain different parts of the Node.js application.

<h5>COPY config.js /app/, COPY server.js /app/, COPY seed.js /app/:</h5> Copies specific files (config.js, server.js, seed.js) from the host machine to the /app directory inside the container. These files likely include configuration settings, the main server file, and a file for seeding data, respectively.

<h5>EXPOSE 5000:</h5> Exposes port 5000 within the container, indicating that the container will listen for incoming connections on this port.

<h5>ENTRYPOINT ["npm", "start"]:</h5> Specifies the command to start the application within the container. In this case, it runs npm start, which likely starts the Node.js server defined in server.js or a similar file.
