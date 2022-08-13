# step 1
FROM alpine

# step 2 install software
RUN echo 'http://dl-cdn.alpinelinux.org/alpine/v3.6/main' >> /etc/apk/repositories 
RUN echo 'http://dl-cdn.alpinelinux.org/alpine/v3.6/community' >> /etc/apk/repositories 
RUN apk update 
RUN apk add mongodb=3.4.4-r0

RUN mongo --version

# step 2.5 configure sw
VOLUME [ "/data/db" ] 
WORKDIR /data 
EXPOSE 27017

# step 3 default command
CMD [ "mongod" ]