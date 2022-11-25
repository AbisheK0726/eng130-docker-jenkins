# Get the mongo image
FROM mongo
# Create a directory for the database
WORKDIR /usr/src/db/
# Copy the mongo configuration file to the image
COPY ./mongod.conf /etc/
# Export the port for the database
EXPOSE 27017
# Start the database
CMD ["mongod"]

