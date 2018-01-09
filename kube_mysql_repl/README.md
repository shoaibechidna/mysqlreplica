# MySQL replication in Kubernetes

Use the slave2 yaml file and deploy in kubernetes

# Check master databases first

> kubectl exec -it --pod='master-pod' --namespace mysql-poc -- mysql -u root -proot -e "show databases"

# For two slave replicas
> kubectl exec -it --pod='slave-pod1' --namespace mysql-poc -- mysql -u root -proot -e "show databases"

> > kubectl exec -it --pod='slave-pod2' --namespace mysql-poc -- mysql -u root -proot -e "show databases"

Here we can see the databases have been replicated.
