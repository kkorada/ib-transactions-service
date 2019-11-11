FROM adoptopenjdk:11-jre-hotspot

ENV IB_SLEEP 0

# add directly the war
ADD *.war /app.war

RUN sh -c 'touch /app.war'
VOLUME /tmp
EXPOSE 8083
CMD echo "The application will start in ${IB_SLEEP}s..." && \
    sleep ${IB_SLEEP} && \
    java -Djava.security.egd=file:/dev/./urandom -jar /app.war