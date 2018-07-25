#### Maximum reference
kubectl [reference](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands) and [cheat sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

---
#### Comandos básicos

1. Aplicando no cluster *(deploying no minikube)* as diretivas *(serviços/instancias)* do arquivo de configuração .yaml:
```
kubectl -f apply ./deployment.yaml
```

1. Expondo a porta do serviço no cluster *(ou seja, o container deixa de ser um "pod" para ser um "serviço")*:
```
kubectl expose deployment tomcat-deployment --type=NodePort
```
1. Descobrindo qual porta foi aberta no cluster para acessar o serviço:
```
minikube service tomcat-deployment --url
```

1. Listando todos os pods presente no cluster:
```
kubectl get pods
```

1. Adquirindo informações detalhadas sobre determinado pod:
```
kubectl describe pod [pod-name]
```

1. Executando comandos nos pods com ***exec*** *(Acessado o shell)*:
```
kubectl exec -it [pod-name] bash
```

1. Rodando um pod no cluster a partir de uma imagem qualquer:
```
kubectl run my-nginx --image=nginx:1.13 --port=8000
```

1. Deletando o pod criado anteriormente *(deve-se informar o namespace do qual faz parte)*:
```
kubectl delete deployment my-nginx --namespace=default
```
