FROM debian:13.4

RUN apt update -y && \
  apt install -y \
  git \
  curl

COPY ./tools ./tools

RUN sh ./tools/install-claude-code.sh
ENV PATH=$PATH:/root/.local/bin

RUN sh ./tools/install-go.sh
ENV PATH=$PATH:/usr/local/go/bin

RUN sh ./tools/install-gopls.sh
