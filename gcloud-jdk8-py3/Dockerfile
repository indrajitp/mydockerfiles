FROM google/cloud-sdk:328.0.0-slim
#RUN apt-get update && apt-get install -y --no-install-recommends rpm
USER root
RUN apt-get update && \
apt-get install -y --no-install-recommends make rpm procps \
&& curl \
        -L \
        -o openjdk.tar.gz \
        https://download.java.net/java/GA/jdk11/13/GPL/openjdk-11.0.1_linux-x64_bin.tar.gz \
    && mkdir jdk \
    && tar zxf openjdk.tar.gz -C jdk --strip-components=1 \
    && rm -rf openjdk.tar.gz \
    && apt-get -y --purge autoremove curl \
    && ln -sf /opt/jdk/bin/* /usr/local/bin/ \    
RUN ln -sf /usr/bin/python3 /usr/bin/python && \
    ln -sf /usr/bin/pip3 /usr/bin/pip
ENTRYPOINT ["tail"]
CMD ["-f","/dev/null"]
