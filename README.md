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
- 
