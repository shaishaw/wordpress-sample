# wordpress-sample : Quickly setup a sample wordpress application on k8s minikube/docker-desktop
Ref: https://kubernetes.io/docs/tutorials/stateful-application/mysql-wordpress-persistent-volume/

Quick wordpress setup

Clone/Download the repository.

$ cd wordpress
$ kubectl create ns app
$ kubectl apply -k ./
  secret/mysql-pass-b6tk659khg created
  service/wordpress created
  service/wordpress-mysql created
  persistentvolumeclaim/mysql-pv-claim created
  persistentvolumeclaim/wp-pv-claim created
  deployment.apps/wordpress created
  deployment.apps/wordpress-mysql created

http://localhost

cleanup 
$ kubectl delete -k ./
