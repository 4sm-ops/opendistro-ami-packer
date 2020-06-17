# opendistro-ami-packer
Open Distro for Elasticsearch

I use following installation guidelines:

https://opendistro.github.io/for-elasticsearch-docs/docs/install/deb/

https://opendistro.github.io/for-elasticsearch-docs/docs/kibana/

ToDo:
1. Change default password:

**Tools location:**
cd /usr/share/elasticsearch/plugins/opendistro_security/tools

**Generate hash:**
sudo bash hash.sh

**Update hash here:**
sudo vi /usr/share/elasticsearch/plugins/opendistro_security/securityconfig/internal_users.yml

**Update configuration:**
sudo bash securityadmin.sh -cd ../securityconfig/ -icl -nhnv -cacert /etc/elasticsearch/root-ca.pem -cert /etc/elasticsearch/kirk.pem -key /etc/elasticsearch/kirk-key.pe
