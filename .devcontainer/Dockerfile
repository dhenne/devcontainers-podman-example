FROM debian:stable-slim

RUN apt update && \
	apt install -y git openssh-client pipenv zsh python3 vim && \
	useradd -m -d /home/user -s /bin/zsh user && \
    mkdir -p /workspaces && \
	chown user:user /workspaces

ARG USERNAME=user
USER $USERNAME

RUN touch ~/.zshrc && \
    echo "[[ ${PIPENV_ACTIVE} -ne 1 ]] && pipenv shell" >> ~/.zshrc
