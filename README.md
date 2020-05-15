## Usefull commands 

##### Start kafka platform :
	docker-compose up -d
##### Stop kafka platform:
	docker-compose stop
##### Recreate container:
	docker-compose up -d --force-recreate --build
##### Create new topic 
	docker-compose exec kafka kafka-topics --create --topic <name of a topic>  --partitions 4 --replication-factor 1 --if-not-exists --zookeeper zookeeper:2181
##### List all topics 
	docker-compose exec kafka kafka-topics --list  --zookeeper zookeeper:2181