# Comandos-kubernetes

- kubectl apply -f DIRETORIO/AQUIVO.yaml ---> faz o deployment da aplicação
- kubeclt get pod ---> visualiza os pod criado do deployment
- kubectl port-forward pod/NOME_CONTAINER 8000:80 ---> Pod acessa a porta 8000 que é direcionada para 80 sem ser preciso criar a network
