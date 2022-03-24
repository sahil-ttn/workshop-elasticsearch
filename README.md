<!------------ Elasticsearch Cluster ------------>

# Prerequisites
- a machine with enough RAM (at least 8 gb)
- `docker` and `docker-compose` installed 

# To start the containers either use
- docker-compose up -d
Now wait for `1 minute`, after that run
- docker ps
It will now be showing the container status as `healthy`

# Confirm that elasticsearch is healthy by visiting one of the following links from your browser or a tool like curl
Elasticsearch nodes:
- [cluster health](http://localhost:9200/_cluster/health?pretty=true)
- [cluster nodes](http://localhost:9200/_nodes/_all/http?pretty=true)
- [master-node health](http://localhost:9200/_cat/health)
- [datanode1 health](http://localhost:9201/_cat/health)
- [datanode2 health](http://localhost:9202/_cat/health)

# To stop the comtainers use
- docker-compose down

# For clean up use
- docker-compose down -v

<!------------ Cerebro ------------>

# To start the cerebro
Extract the cerebro.zip file
- unzip cerebro.zip
Go inside the ./cerebro/bin directory
- bash cerebro

# Acessing the cerebro page
Go to the browser and type
http://localhost:9000
Now you will land to the cluster login page, type the following url:
http://localhost:9200
And now can access the master web ui of elasticsearch cluster
