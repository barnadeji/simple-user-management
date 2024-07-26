FROM node:18.13.0-alpine

ENV ENVIRONMENT=""

RUN apk add --update vim && \
    addgroup bdeji && adduser -s /bin/sh -G bdeji -D bdeji

ENV HOME /home/bdeji

RUN mkdir -p $HOME && chown -R bdeji:bdeji $HOME

WORKDIR $HOME/app

RUN chown -R bdeji:bdeji $HOME/app/

USER bdeji

COPY --chown=bdeji:bdeji package*.json ./

RUN npm install

EXPOSE 3000

COPY --chown=bdeji:bdeji . .

ENTRYPOINT ["npm", "start"]