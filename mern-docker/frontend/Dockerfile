#sets base image to create image for react app
FROM node:20-alpine
#set the working directory to /app
WORKDIR /app
#copy json package to workdir
COPY package*.json ./
#install dependencies
RUN npm install
#copy rest of files to workdir
COPY . .
#expose port 5173 telling docker that container listens on specific port number
EXPOSE 5173
#command to run app
CMD npm run dev