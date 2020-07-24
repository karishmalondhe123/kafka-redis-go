FROM golang
RUN mkdir /work
WORKDIR /work/
RUN git clone https://gitlab.com/melwyn95/go-redis-kafka-demo.git
RUN chmod 777 go-redis-kafka-demo/start.sh
WORKDIR go-redis-kafka-demo/
CMD [ "bash", "-c" , "./start.sh"]
