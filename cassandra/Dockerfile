FROM cassandra:4.0.1
# RUN cat "${CASSANDRA_HOME}/conf/logback.xml"
# Sets log level to WARN instead of default INFO
COPY ./logback.xml "${CASSANDRA_HOME}/conf"