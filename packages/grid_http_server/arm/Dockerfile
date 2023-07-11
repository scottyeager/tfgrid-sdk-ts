FROM alpine

ARG GRID_VERSION
RUN apk add nodejs npm curl python3 build-base && npm install --global yarn && yarn add @threefold/grid_http_server@${GRID_VERSION}

ENTRYPOINT [ "yarn" ]
