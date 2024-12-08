# DevOps

Task 1 postgres cluster:

Creating the postgres cluster:
here is the functions that were used for its creation:

Check the existence of he stateful states:
kubectl get sts
kubectl get pv

Creating the yamls for creating the postgres sets
vim postgresVolume.yml
vim postgres-service.yml
vim postgres-statefulset.yml

create the yaml for the postgres

applying the configurations for sts:
kubectl apply -f postgresVolume.yml
kubectl apply -f postgres-service.yml  
kubectl apply -f postgres-statefulset.yml

get description
kubectl describe pv pv-data-postgres-0

creating the postgress service:
vim postgres-service.yml

Important:
Add port to the security rules on AWS:
EC -> running instances-> click on node-> Security-> add rule

Here we check out postgres sts:

1. Task1: nginx was automaticall installed via bash script by using the provision in the vagrant file.
   ![2_replicas](https://github.com/Alex-Sigma/Development/blob/lecture18/images/2_replicas_postgres.png)

![running_postgres](https://github.com/Alex-Sigma/Development/blob/lecture18/images/Postgres_running.png)

![persistent_volums](https://github.com/Alex-Sigma/Development/blob/lecture18/images/persistent_volumes.png)

![persistent_volume_2](https://github.com/Alex-Sigma/Development/blob/lecture18/images/postgred_cluster.png)
