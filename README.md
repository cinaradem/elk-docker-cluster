git clone https://github.com/cinaradem/elk-docker-cluster.git
ELASTICSEARCH_DATA="/elastic/"
mkdir $ELASTICSEARCH_DATA
sudo chown -R 1000:1000 $ELASTICSEARCH_DATA
sudo chmod +x install.sh
.\install.sh

sudo nano /etc/sysctl.conf
vm.max_map_count = 262144
sudo reboot

## Run
`docker-compose up -d`



curl -XPOST 'localhost:9200/my_index/my_type/_update_by_query?conflicts=proceed&wait_for=true'
