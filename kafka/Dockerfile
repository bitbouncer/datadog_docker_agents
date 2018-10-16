# Agent running a kafka monitoring
FROM datadog/docker-dd-agent

# Install JMXFetch dependencies
RUN apt-get update \
&& apt-get install openjdk-8-jdk-headless -qq --no-install-recommends

#override the original so we can run with broken api_keys 
ADD config.py /opt/datadog-agent/agent/config.py

# Add kafka check configuration
ADD kafka.yaml /etc/dd-agent/conf.d/kafka.yaml





