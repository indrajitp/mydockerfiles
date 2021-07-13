FROM python:3.8-slim-buster
#RUN apt-get update && apt-get install -y --no-install-recommends rpm
RUN mkdir -p /usr/share/man/man1 /usr/share/man/man2

USER root
RUN apt-get update && \
apt-get install -y --no-install-recommends make rpm procps openjdk-11-jre  
RUN ln -sf /usr/bin/python3 /usr/bin/python && \
    ln -sf /usr/bin/pip3 /usr/bin/pip
    
ENTRYPOINT ["tail"]
CMD ["-f","/dev/null"]
