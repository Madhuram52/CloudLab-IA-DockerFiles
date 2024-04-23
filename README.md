# CloudLab-IA-DockerFiles

[ShopJunkieProject- GithubLink](https://github.com/Madhuram52/ShopJunkie)   - This is A MERN Stack Project which I Made Earlier


<h3>Frontend-Dockerfile :</h3>


**FROM node:18:** Specifies the base image as Node.js version 18.

**WORKDIR /app:** Sets the working directory inside the container to /app.

**COPY package.json /app/package.json and COPY package-lock.json /app/package-lock.json:** Copies Node.js project configuration files.

**RUN npm install:** Installs project dependencies.

**COPY src /app/src, COPY public /app/public, COPY index.html /app/, COPY README.md /app/, COPY vite.config.js /app/:** Copies project source code and configuration files.

**EXPOSE 5173:** Exposes port 5173 for external connections.

**ENTRYPOINT ["npm", "run", "dev"]:** Sets the command to start the application as npm run dev.


<h3>Backend-DockerFile : </h3>

**FROM node:18:** Specifies the base image as Node.js version 18.

**WORKDIR /app:** Sets the working directory inside the container to /app. All subsequent commands will be executed relative to this directory.

**COPY package.json /app/package.json and COPY package-lock.json /app/package-lock.json:** Copies Node.js project configuration files.

**RUN npm install:** Installs project dependencies based on the package.json and package-lock.json files.

**COPY controllers /app/controllers, COPY middleware /app/middleware, COPY models /app/models, COPY routes /app/routes:** Copies various directories (controllers, middleware, models, routes) from the host machine to corresponding directories inside the container's /app directory. These likely contain different parts of the Node.js application.

**COPY config.js /app/, COPY server.js /app/, COPY seed.js /app/:** Copies specific files (config.js, server.js, seed.js) from the host machine to the /app directory inside the container. These files likely include configuration settings, the main server file, and a file for seeding data, respectively.

**EXPOSE 5000:** Exposes port 5000 within the container, indicating that the container will listen for incoming connections on this port.

**ENTRYPOINT ["npm", "start"]:** Specifies the command to start the application within the container. In this case, it runs npm start, which likely starts the Node.js server defined in server.js or a similar file.
