sudo yum install git

git clone https://github.com/cinaradem/elk-docker-cluster.git
ELASTICSEARCH_DATA="/elastic/"
sudo rm -rf $ELASTICSEARCH_DATA
sudo mkdir $ELASTICSEARCH_DATA
sudo chown -R 1000:1000 $ELASTICSEARCH_DATA
sudo chmod +x install.sh
.\install.sh

sudo nano /etc/sysctl.conf

sudo reboot



ilk kurulumda da kapat       - xpack.security.transport.ssl.enabled=true
sonra aç
## Run
sudo docker-compose up es2
sudo docker-compose up -d docker40
gi
sudo docker-compose stop
sudo docker-compose rm -f
git stash
git pull
sudo docker-compose up es1

curl -XPOST 'localhost:9200/my_index/my_type/_update_by_query?conflicts=proceed&wait_for=true'
