# Agent running a kafka monitoring
FROM datadog/docker-dd-agent

# Install JMXFetch dependencies
RUN apt-get update \
&& apt-get install openjdk-8-jdk-headless -qq --no-install-recommends

# Add kafka check configuration
ADD kafka.yaml /etc/dd-agent/conf.d/kafka.yaml

ADD metrics.yaml /etc/dd-agent/conf.d/metrics.yaml

ADD config.py /opt/datadog-agent/agent/config.py



