## Usefull commands 

#####  Adding ACLs :
	docker-compose exec kafka kafka-acls  --authorizer kafka.security.auth.SimpleAclAuthorizer --authorizer-properties zookeeper.connect=zookeeper:2181 --add --allow-principal User:<user_name> --allow-hosts * --operation Read --topic <topic_name>

##### List ACls for topic:
	docker-compose exec kafka kafka-acls  --authorizer kafka.security.auth.SimpleAclAuthorizer --authorizer-properties  zookeeper.connect=zookeeper:2181  --list --topic <topic_name>
##### Add consumer:
	docker-compose exec kafka kafka-acls  --authorizer kafka.security.auth.SimpleAclAuthorizer --authorizer-properties zookeeper.connect=zookeeper:2181 --add --allow-principal User:<user_name> --consumer --topic <topic_name> --group <group_name>