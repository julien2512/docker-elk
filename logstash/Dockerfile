FROM logstash:latest

RUN mkdir data

RUN apt-get update
RUN apt-get -y install git
RUN git clone https://github.com/regardscitoyens/reporting_international.git /data

RUN logstash-plugin install logstash-filter-grok
RUN logstash-plugin install logstash-filter-drop
RUN logstash-plugin install logstash-filter-mutate
RUN logstash-plugin install logstash-filter-csv

# Add your logstash plugins setup here
# Example: RUN logstash-plugin install logstash-filter-json 
