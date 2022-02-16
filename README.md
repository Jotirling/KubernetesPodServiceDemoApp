# KubernetesPodServiceDemoApp

Kuberneter Voting Demo App using pod and services *.yml

Clone the Repo in Kubectl environment and run the below commands:

$ kubectl create -f voting-app-pod.yml

$ kubectl create -f voting-app-service.yml

$ kubectl create -f redis-pod.yml

$ kubectl create -f redis-service.yml

$ kubectl create -f worker-app-pod.yml

$ kubectl create -f postgres-pod.yml

$ kubectl create -f postgres-service.yml

$ kubectl create -f result-app-pod.yml

$ kubectl create -f result-app-service.yml

$ minikube service list

|-------------|----------------|--------------|-----------------------------|
|  NAMESPACE  |      NAME      | TARGET PORT  |             URL             |
|-------------|----------------|--------------|-----------------------------|
| default     | db             | No node port |                             |
| default     | kubernetes     | No node port |                             |
| default     | redis          | No node port |                             |
| default     | result-service |           80 | http://192.168.59.100:30002 |
| default     | voting-service |           80 | http://192.168.59.100:30001 |
| kube-system | kube-dns       | No node port |                             |
|-------------|----------------|--------------|-----------------------------|

Check the IP address for the service might be differnet in your case.
Open your brower and hit the above two ip address to access 
<voting-app>
http://192.168.59.100:30001 
<result-app>
http://192.168.59.100:30002
