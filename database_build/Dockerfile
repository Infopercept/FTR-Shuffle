FROM opensearchproject/opensearch:latest

USER root
RUN usermod -u 1010 opensearch
RUN groupmod -g 1010 opensearch
RUN find . -uid 1000 -exec chown 1010:1010 {} +

RUN ls -l
RUN chown opensearch:opensearch "opensearch-docker-entrypoint.sh"

ARG UID=1010
ARG GID=1010
USER 1010

CMD ["./opensearch-docker-entrypoint.sh"]
