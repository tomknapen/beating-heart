FROM nodered/node-red:latest

# install stuff that need sudo rights
USER root

# install node-red-admin which is needed if you want to created hashed password for the node-red editor.
RUN  npm install -g --unsafe-perm node-red-admin

# install 
USER node-red

COPY ./settings.js /data/settings.js

# plugins
RUN cd /data

RUN npm install node-red-dashboard

RUN npm install node-red-contrib-credentials
RUN npm install node-red-contrib-state-machine
RUN npm install node-red-contrib-telegrambot-home
RUN npm install node-red-contrib-time-range-switch
RUN npm install node-red-contrib-webhookrelay
