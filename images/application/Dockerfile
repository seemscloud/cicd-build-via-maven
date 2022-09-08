FROM nginx:latest
LABEL Mainteiner="mateusz.adam.katana@gmail.com"

ARG APP_VERSION
ARG APP_USER
ARG APP_GROUP
ARG APP_UID
ARG APP_GUID

ARG APP_DIR="/app"

RUN mkdir -p "${APP_DIR}"

RUN echo "${APP_VERSION}" >> version.txt