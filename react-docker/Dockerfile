#sets base image to create image for react app
FROM node:20-alpine
#create new user with perms to run the app
RUN addgroup app && adduser -S -G app app
#set user to run the app
USER app
#set the working directory to /app
WORKDIR /app
#copy json package to workdir
COPY package*.json ./
#change ownership of files to root user
USER root
#change ownership of /app dir to the app user
RUN chown -R app:app .
#change user back to app user
USER app
#install dependencies
RUN npm install
#copy rest of files to workdir
COPY . .
#expose port 5173 telling docker that container listens on specific port number
EXPOSE 5173
#command to run app
CMD npm run dev