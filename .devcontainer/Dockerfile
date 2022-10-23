FROM mono:latest

ENV NODE_VERSION=16.13.0
RUN apt install -y curl
RUN curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash
ENV NVM_DIR=/root/.nvm
RUN . "$NVM_DIR/nvm.sh" && nvm install ${NODE_VERSION}
RUN . "$NVM_DIR/nvm.sh" && nvm use v${NODE_VERSION}
RUN . "$NVM_DIR/nvm.sh" && nvm alias default v${NODE_VERSION}
ENV PATH="/root/.nvm/versions/node/v${NODE_VERSION}/bin/:${PATH}"
RUN node --version
RUN npm --version


RUN curl -o- -L https://dot.net/v1/dotnet-install.sh | bash -s -- -c Current
RUN ln -s /root/.dotnet/dotnet /usr/bin/dotnet
# Install Latest Git version
RUN apt-get install -y software-properties-common && add-apt-repository ppa:git-core/ppa
RUN apt-get update && apt-get install -y git
RUN apt-get install -y vim
RUN git config --global core.editor "vim"

RUN apt-get update -y && apt-get install -y mono-xsp4

RUN bash -c "$(curl -fsSL https://raw.githubusercontent.com/ohmybash/oh-my-bash/master/tools/install.sh)"
