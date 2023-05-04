FROM goreleaser/goreleaser:latest as goreleaser

FROM ubuntu:latest

RUN export DEBIAN_FRONTEND=noninteractive \
    && apt-get update \
    && apt-get install \
      --no-install-recommends \
      --yes \
      git

COPY --from=goreleaser /usr/bin/goreleaser /usr/bin/goreleaser
