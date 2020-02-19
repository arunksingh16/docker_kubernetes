# Readme 

- Creating a pod via command

kubectl run pod1 --image=arun161087/docker-http-server --generator=run-pod/v1 --dry-run

kubectl run pod1 --image=arun161087/docker-http-server --generator=run-pod/v1

kubectl label pods pod1 env=dev


- Creating a pod via Yaml file

kubectl create -f pod.yaml

-  Pod Operation 

kubectl get pods
kubectl get pods -o wide
kubectl describe pod <pod-name>
kubectl get pods -o wide --show-labels --all-namespaces
kubectl delete pods 

- Create a Service 

kubectl create -f service.yaml
kubectl get services

- Create a RS

kubectl create -f rs.yaml
kubectl scale --replicas=3 rs/rs
kubectl delete replicaset rs

- Delete a POD in RS

kubectl delete pod <pod>

- Create a Deployment

kubectl create -f dep.yaml

(The pod-template-hash label is added by the Deployment controller to every ReplicaSet that a Deployment creates or adopts. This label ensures that child ReplicaSets of a Deployment do not overlap.)


kubectl apply -f dpl.yaml  (update image name as nginx)

kubectl set image deployment/dep nginx 

kubectl autoscale deployment dep 3

kubectl rollout history deployment/dep

kubectl rollout status -w deployments/dep

kubectl rollout history deployment/dep --revision=2

kubectl rollout undo deployment/dep --to-revision=1

kubectl create deployment nginx --image=nginx

- Labels and Selectors

kubectl get pods  -l tier=frontend

kubectl get pods  -l env!=prod,tier=backend

(In above commands, labels separated by comma is a kind of AND satisfy operation.)

kubectl get pod -l 'env in (dev)'


# Other Supported command 

kubectl get nodes

kubectl describe nodes

kubectl get namespace

kubectl get pods --all-namespaces


kubectl run nginx --image=nginx --restart=Never --dry-run -o yaml > pod.yaml    # Run pod nginx and write its spec into a file called pod.yaml
