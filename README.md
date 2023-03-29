# assignment-1


# Step 1 (5 marks): Identify a Sample Application

Hello World In Node.Js
App.Js File

const http = require('http');
const hostname = '0.0.0.0';
const port = 3000;

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello, World!\n');
});

server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});

# Step 2 (5 marks): Identify the Dependencies

NPM

# Step 3 (15 marks): Create a Dockerfile
Dockerfile
FROM node:14-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 3000
CMD [ "npm", "start" ]

# Step 4 (25 marks): Build the Docker Image

Docker build -t mrbasit01/myapp:latest

# Step 5 (25 marks): Push the Docker Image to DockerHub

Docker push mrbasit01/myapp:latest

# Step 6 (10 marks): Create a GitHub Repository

# Step 7 (15 marks): Include a README.md file

# Step 8 (5 marks): Push the Codebase to GitHub

