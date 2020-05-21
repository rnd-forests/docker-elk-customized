ARG ELK_VERSION

# https://www.docker.elastic.co/
FROM docker.elastic.co/logstash/logstash:${ELK_VERSION}

COPY mysql-connector-java-8.0.16.jar /usr/share/logstash
ADD mysql-connector-java-8.0.16.jar logstash-core/lib/jars/

# Add your logstash plugins setup here
# Example: RUN logstash-plugin install logstash-filter-json
