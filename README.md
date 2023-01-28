# Comandos-kubernetes

- kubectl apply -f DIRETORIO/AQUIVO.yaml ---> faz o deployment da aplicação
- kubeclt get pod ---> visualiza os pod criado do deployment
- kubectl port-forward pod/NOME_CONTAINER 8000:80 ---> Pod acessa a porta 8000 que é direcionada para 80 sem ser preciso criar a network
- kubectl delete pod NOME_CONTAINER ---> deleta o pod
- kubectl get replicasets ---> verifica quantas replicacas o container tem
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

