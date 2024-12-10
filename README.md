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

![2_replicas](https://github.com/Alex-Sigma/Development/blob/lecture18/images/2_replicas_postgres.png)

![running_postgres](https://github.com/Alex-Sigma/Development/blob/lecture18/images/Postgres_running.png)

![persistent_volums](https://github.com/Alex-Sigma/Development/blob/lecture18/images/persistent_volumes.png)

![persistent_volume_2](https://github.com/Alex-Sigma/Development/blob/lecture18/images/postgred_cluster.png)

Task 2

creating the Falco

1. First with the deployment instructions in yaml were created.
   It can be found in the file yaml with the name falco-daemonset.yaml.

2. Afterwards the the service was deployed with kubectl apply -f falco-daemonset.yaml

3. The results of the deployment can be checked with kubectl logs -l app=falco -n kube-system

![Falco_Creation](https://github.com/Alex-Sigma/Development/blob/lecture18/images/Creating_Falco_yml_deployment.png)

![Output_pods](https://github.com/Alex-Sigma/Development/blob/lecture18/images/Falco_Pods.png)

There were probably problema with the space, that is why one of the pods was evicted.
Open to the suggestions on how to avoid it.
