#  Copyright (c) Microsoft Corporation. All rights reserved.
#  Licensed under the MIT License. See License.txt in the project root for license information.

FROM debian:stable-slim

RUN apt update && \
	apt install -y git openssh-client pipenv zsh python3 && \
	useradd -m -d /home/user -s /bin/zsh user && \
    mkdir -p /workspaces && \
	chown user:user /workspaces

ARG USERNAME=user
USER $USERNAME

RUN touch ~/.zshrc && \
    echo "pipenv shell" >> ~/.zshrc
