# Comandos-kubernetes

- kubectl apply -f DIRETORIO/AQUIVO.yaml ---> faz o deployment da aplicação
- kubeclt get pod ---> visualiza os pod criado do deployment
- kubectl port-forward pod/NOME_CONTAINER 8000:80 ---> Pod acessa a porta 8000 que é direcionada para 80 sem ser preciso criar a network
- kubectl delete pod NOME_CONTAINER ---> deleta o pod
- kubectl get replicasets ---> verifica quantas replicas o container tem
- kubectl rollout history deployment NOME_CONTAINER ---> Ver quantas revisões foram feitas
- kuberctl rollout undo deployment NOME_CONTAINER ---> Volta para última revisão anteriomente atualizada
- kuberctl rollout undo deployment NOME_CONTAINER --to-revidion=NÚMERO_DA_REVISÃO ---> Vai para versão específicada
- kubectl describe deployment NOME_CONTAINER ---> Mostra vários detalhes do container
- kubectl get service ou svc ---> Vizualiza os serviços que estão rodando
- kubectl port-forward svc/NOME_DO_SERVICE 8000:80 ---> a porta 8000 que é direcionada para 80 para ter acesso ao SERVICE
- kubectl proxy --port=8080 ---> Consegui vizualizar as APIs do kubernetes ao acessar localhost:8080
- kubectl exec -it NOME_CONTAINER/POD -- bash ---> Acessa o container
- kubectl logs NOME_CONTAINER ---> Verifica os logs do container
- kubectl apply -f DIRETORIO/AQUIVO.yaml && watch -n1 kubectl get pods ---> Faz o apply e já verifica em tempo real os pods rodando
- kubectl get apiservices --->Lista todos serviços que temos na API
- kubectl top pod NOME_CONTAINER ---> trás o consumo de CPU e memória do pod
- kubectl get hpa ---> verifica os hpa
- kubectl run -it fortio --rm --image=fortio/fortio -- load -qps 800 -t 120s -c 70 "http://goserver-service/healthz" ---> será possível ver os pods escalando no teste de stress
- kubectl get storageclass ---> Mostra o storage atrelado ao cluster
- kubectl config get-contexts ---> Mostra todos cluster
- kubectl config use-context NOME_CLUSTER ---> Entra no cluster específico
- kubectl delete deploy NOME_DO_POD ---> mata todos pods
- kubectl delete statefulset NOME_DO_POD ---> Deleta os pod criado como statefulset
- kubectl scale statefulset  NOME_DO_POD --replicas=5 ---> Cria pods em paralelo (sendo que o spec fica --> podManagementPolicy:parallel)
- kubectl get pvc ---> visualiza os volumes no cluster atual
- kubectl create namespace cert-manager ---> Cria o namespace chamado cert-manager
- kubectl get ns ---> vizualiza os namespace
- kubectl describe certificate NOME_DO_CERTIFICADO ---> Verifca a descrição do certificado
- kubectl apply -f DIRETORIO/AQUIVO.yaml -n=NOME_DO_NAMASPACE ---> Faz o apply no namespace específico
- kubectl config view---> Visualiza as configurações usada no cluster
- kubectl config current-context ---> Vizualiza o contexto do cluster atual
- kubectl get serviceaccounts ---> mostra o serviceaccounts que contém as permissões da aplicação
- kubectl api-resources ---> visualiza nome das APIs e apiGROUPS

# Liks Documentação Kubernetes

- https://kubernetes.io/pt-br/docs/home/
- https://kubernetes.io/pt-br/docs/setup/production-environment/tools/kops/
- https://kubernetes.io/pt-br/docs/setup/production-environment/tools/kubeadm/install-kubeadm/
- https://cert-manager.io/docs/installation/kubectl/ ---> Instalar certificado ssl para uso do https

# Nginx ingress controller
- https://docs.nginx.com/nginx-ingress-controller/installation/installation-with-helm/

# Comandos utilizado no Curso de kubernetes - Full Cycle -> Wesley Willians





