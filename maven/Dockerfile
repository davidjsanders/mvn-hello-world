FROM        ubuntu:18.04
RUN         apt-get update \
            && apt-get install --yes openjdk-8-jdk
RUN         apt-get update \
            && apt-get install --yes \
                apt-transport-https \
                ca-certificates \
                curl \
                maven \
                net-tools
#ADD         https://download.java.net/java/GA/jdk11/13/GPL/openjdk-11.0.1_linux-x64_bin.tar.gz /tmp/openjdk-11.0.1_linux-x64_bin.tar.gz
WORKDIR     /tmp
RUN         curl --output openjdk-11.0.1_linux-x64_bin.tar.gz https://download.java.net/java/GA/jdk11/13/GPL/openjdk-11.0.1_linux-x64_bin.tar.gz \
            && tar xvf openjdk-11.0.1_linux-x64_bin.tar.gz \
            && mv jdk-11.0.1 /usr/lib/jvm/
WORKDIR     /root
VOLUME      ["my-app"]
ENTRYPOINT  ["bash"]
