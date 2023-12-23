ARG BUILD_FROM=ghcr.io/hassio-addons/debian-base:7.3.0

# https://github.com/hassio-addons/addon-base/releases
# hadolint ignore=DL3006
FROM ${BUILD_FROM}

# https://github.com/eikek/sharry/releases
ARG MONEROD_VERSION=v0.18.3.1

# Add monerod
RUN set -eux; \
    apt-get update; \
    \
    apt-get --no-install-recommends -y install \
        bzip2=1.0.8-5+b1 \
        ; \
    mkdir -p /opt; \
    curl -s -J -L -o /tmp/monerod.tar.bz2 \
        "https://downloads.getmonero.org/cli/monero-linux-armv8-${MONEROD_VERSION}.tar.bz2"; \
    tar -xjf /tmp/monerod.tar.bz2 -C /tmp; \
    apt-get -y autoremove --purge \
        bzip2 \
        ; \
    apt-get clean; \
    rm -rf /var/lib/apt/lists/*; \
    mv /tmp/monero-aarch64-linux-gnu-${MONEROD_VERSION}/monerod /opt/monerod; \
    rm /tmp/monerod.tar.bz2; \
    rm -r /tmp/monero-aarch64-linux-gnu-${MONEROD_VERSION}
    
COPY --chmod=445 rootfs /
WORKDIR /

# Build arguments
ARG BUILD_ARCH
ARG BUILD_DATE
ARG BUILD_DESCRIPTION
ARG BUILD_NAME
ARG BUILD_REF
ARG BUILD_REPOSITORY
ARG BUILD_VERSION

# Labels
LABEL \
    io.hass.name="${BUILD_NAME}" \
    io.hass.description="${BUILD_DESCRIPTION}" \
    io.hass.arch="${BUILD_ARCH}" \
    io.hass.type="addon" \
    io.hass.version=${BUILD_VERSION} \
    maintainer="Frosh" \
    org.opencontainers.image.title="${BUILD_NAME}" \
    org.opencontainers.image.description="${BUILD_DESCRIPTION}" \
    org.opencontainers.image.vendor="Frosh Home Assistant Add-ons" \
    org.opencontainers.image.authors="Frosh" \
    org.opencontainers.image.licenses="MIT" \
    org.opencontainers.image.url="https://github.com/erdnaxela02/hassio-addons" \
    org.opencontainers.image.source="https://github.com/${BUILD_REPOSITORY}" \
    org.opencontainers.image.documentation="https://github.com/${BUILD_REPOSITORY}/blob/main/README.md" \
    org.opencontainers.image.created=${BUILD_DATE} \
    org.opencontainers.image.revision=${BUILD_REF} \
    org.opencontainers.image.version=${BUILD_VERSION}
