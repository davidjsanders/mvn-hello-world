FROM ubuntu:18.04
RUN         apt-get update \
            && apt-get install --yes openjdk-8-jdk
RUN         apt-get update \
            && apt-get install --yes \
                apt-transport-https \
                ca-certificates \
                chromium-browser \
                cron \
                curl \
                gettext \
                gpg \
                git \
                iptables \
                lxc \
                maven \
                net-tools \
                python3.7 \
                python-pip \
                software-properties-common \
                sudo \
                unzip \
            && groupadd docker \
            && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - \
            && add-apt-repository \
                "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
                $(lsb_release -cs) \
                stable" \
            && apt-get update \
            && apt-get install docker-ce -y \
            && curl -sL https://deb.nodesource.com/setup_9.x | sudo -E bash - \
            && apt-get install nodejs -y \
            && npm install -g @angular/cli \
            && npm install -g n \
            && npm install -g sonarqube-scanner \
            && npm install -g webpack@4.8.1 \
            && npm install -g webpack-cli@2.1.3 \
            && npm install -g yarn
VOLUME ["my-app"]
ENTRYPOINT ["bash"]
CMD []
