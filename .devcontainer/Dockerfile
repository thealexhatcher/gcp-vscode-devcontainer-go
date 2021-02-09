FROM google/cloud-sdk:latest
RUN apt-get update && apt-get install -y \
        build-essential \
        golang \
        zip 
RUN curl -O "https://releases.hashicorp.com/terraform/0.12.23/terraform_0.12.23_linux_amd64.zip" \
    && unzip terraform_0.12.23_linux_amd64.zip \
    && mv terraform /usr/local/bin/ \
    && terraform --version \
    && rm terraform_0.12.23_linux_amd64.zip
## SYSTEM SETUP
## VSCODE USER Setup
RUN useradd -ms /bin/bash vscode
RUN usermod -aG sudo vscode
USER vscode


