FROM debian:bullseye-slim
LABEL Mainteiner="mateusz.adam.katana@gmail.com"

ARG APP_VERSION
ARG APP_USER
ARG APP_UID
ARG APP_GROUP
ARG APP_GID
ARG APP_DIR="/app"

RUN groupadd --gid "${APP_GID}" "${APP_GROUP}" && \
    useradd --uid "${APP_UID}" --gid "${APP_GID}" --home "${APP_DIR}" "${APP_USER}"

WORKDIR "${APP_DIR}"

RUN mkdir -p src
COPY ./files/source src

RUN chown -R "${APP_USER}":"${APP_GROUO}" "${APP_DIR}"

USER "${APP_USER}"

COPY ./docker-entrypoint.sh .

ENTRYPOINT [ "/bin/bash", "docker-entrypoint.sh" ]
