# docker build --tag shuxs/drone-maven-docker-build:latest . && docker push shuxs/drone-maven-docker-build:latest
FROM shuxs/docker-cli:latest

RUN apk add --no-cache openjdk8 maven; \
    rm -rf /docker /var/lib/apk /etc/apk/cache; \
    java -version; \
    mvn -v;

COPY ./drone-maven-docker-build.sh java.Dockerfile /

CMD [ "/drone-maven-docker-build.sh" ]
