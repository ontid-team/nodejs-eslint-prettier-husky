ARG VARIANT="18"
FROM node:${VARIANT}

# Install basic development tools
RUN apt-get update
RUN apt-get install -y \
  sudo \
  lsb-release \
  curlcu

# Ensure default `node` user has access to `sudo`
ARG USERNAME=node
RUN echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME \
  && chmod 0440 /etc/sudoers.d/$USERNAME

# Set `DEVCONTAINER` environment variable to help with orientation
ENV DEVCONTAINER=true
