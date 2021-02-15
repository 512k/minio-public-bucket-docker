# Image page: <https://hub.docker.com/r/minio/minio>
FROM minio/minio:RELEASE.2021-02-14T04-01-33Z

LABEL \
    org.label-schema.name="minio-public-bucket" \
    org.label-schema.description="minio with automatic public bucket" \
    org.label-schema.url="https://github.com/512k/minio-public-bucket-docker" \
    org.label-schema.vcs-url="https://github.com/512k/minio-public-bucket-docker" \
    org.label-schema.license="MIT" \
    org.label-schema.schema-version="1.0"

COPY ./allow-all-policy.json ./docker-entrypoint.sh /opt/

ENTRYPOINT ["/opt/docker-entrypoint.sh"]
CMD ["server", "/data"]
