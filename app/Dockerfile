FROM node as app
# Create app directory
WORKDIR /usr/src/app
# Install app dependencies
COPY package*.json ./
RUN npm install -g npm@7.20.6
# Copy app source code
COPY . .
# Make port 3000 available to the world outside this container
EXPOSE 3000
# Run the app
CMD ["node", "app.js"]


# New a lightweight image of node
FROM node:alpine
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm install -g npm@7.20.6
# Copy app source code from the previous image
COPY --from=app /usr/src/app /usr/src/app
EXPOSE 3000
CMD ["node", "app.js"]
