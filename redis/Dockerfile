FROM golang
RUN apt-get -y update
RUN apt-get install -y redis-server
RUN mkdir /work
COPY start-app.sh /work/
RUN chmod 777 /work/start-app.sh
CMD ["bash", "-c", "/work/start-app.sh"]
