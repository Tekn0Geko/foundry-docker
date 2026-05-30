
# Run Foundry VTT in a Docker Container

This project is just a couple of folks simply sharing how they setup Docker to run Foundry VTT.
The need for such a setup came about when version 14 dropped support for macOS Monetery.
Hardware was still good but the software lifecycle has moved on from the operating system.
This is the way of sofware, it was anticipated somewhat, and is viewed as a positivie forcing function.

There is no warranty with this solution and no guarantee it will work for you. However, feel free to
submit an issue if you come across a bug or an optimization. This is a for-fun project mainly. Also
keep in mind this approach is one of many. See the resources list below for links to other Foundry
VTT solutions, like just running locally via Node.

# TL;DR

Login to the Foundry VTT main page and download the compressed Node source file.

Copy the compressed Node source file into the `app/` directory supplied in this repo. 

Build the image locally:

`docker-compose build foundryvtt`

Start the container instance as a background service:

`docker-compose up -d foundryvtt`

Stop the instance when done:

`docker-compose stop foundryvtt`

# Resource Links

- [Foundry VTT - main site](https://foundryvtt.com/)
- [Community Wiki - Docker inspiration](https://foundryvtt.wiki/en/setup/hosting/Docker)
- [Foundry VTT Installation Guide](https://foundryvtt.com/article/installation/#dedicated)
- [Foundry VTT Node Configuration Options](https://foundryvtt.com/article/configuration/)
- [Docker Hub Image - Main Inspiration](https://hub.docker.com/r/felddy/foundryvtt)
- [Docker](https://www.docker.com/)
