# Run latest version instance
FROM node:24-alpine

# Create user
RUN adduser -D foundry

# Switch to new user and create FoundryVTT app,data directories
USER foundry
RUN mkdir -p /home/foundry/app

# Note that Docker will mount this directory to local host directory at runtime
RUN mkdir -p /home/foundry/data

# Set app working directory and copy application source file
ENV FOUNDRY_HOME=/home/foundry/app
COPY FoundryVTT-Node-*.zip ${FOUNDRY_HOME}

# Change to app directory as the working directory
WORKDIR "${FOUNDRY_HOME}"

# Unpack FoundryVTT application files
RUN unzip FoundryVTT-Node-*.zip
RUN rm FoundryVTT-Node-*.zip

# Expose default server port
EXPOSE 30000

# Start running the server (FoundryVTT V13 and newer)
CMD ["node", "main.js", "--dataPath=/home/foundry/data" ]
