ARG ELK_VERSION

# https://www.docker.elastic.co/
FROM docker.elastic.co/elasticsearch/elasticsearch:${ELK_VERSION}

COPY elasticsearch-analysis-vietnamese-7.3.1.zip /usr/share/elasticsearch

# Add your elasticsearch plugins setup here
# Example: RUN elasticsearch-plugin install analysis-icu
RUN cd /usr/share/elasticsearch \
    && yes | bin/elasticsearch-plugin install analysis-icu \
    && yes | bin/elasticsearch-plugin install file:///usr/share/elasticsearch/elasticsearch-analysis-vietnamese-7.3.1.zip
