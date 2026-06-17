# DL4000 — MAINTAINER is deprecated
#
# Rules under test: DL4000 (https://github.com/hadolint/hadolint/wiki/DL4000)
#
# The MAINTAINER instruction below is deprecated and produces a DL4000 violation.

FROM ubuntu:22.04

MAINTAINER Jane Doe <jane@example.com>

RUN apt-get update && apt-get install -y --no-install-recommends curl \
    && rm -rf /var/lib/apt/lists/*
