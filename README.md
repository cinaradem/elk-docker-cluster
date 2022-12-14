git clone https://github.com/cinaradem/elk-docker-cluster.git
ELASTICSEARCH_DATA="/elastic/"
sudo chmod +x install.sh
.\install.sh

sudo nano /etc/sysctl.conf
vm.max_map_count = 262144
sudo reboot

## Run
`docker-compose up -d`
