FROM nodered/node-red-docker:rpi-v8

# install stuff that need sudo rights
USER root

# installing an editor
RUN apt-get update && apt-get install nano
# install node-red-admin which is needed if you want to created hashed password for the node-red editor.
RUN  npm install -g --unsafe-perm node-red-admin

# install 
USER node-red

RUN npm install node-red-dashboard
RUN npm install node-red-contrib-credentials

COPY ./settings.js /data/settings.js
