#### Maximum reference
kubectl [reference](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands) and [cheat sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

---
#### Comandos básicos

1. Aplicando no cluster *(deploying no minikube)* as diretivas *(serviços/instancias)* do arquivo de configuração .yaml:
```shell
kubectl -f apply ./deployment.yaml
```

2. Expondo a porta do serviço no cluster *(ou seja, o container deixa de ser um "pod" para ser um "serviço")*:
```shell
kubectl expose deployment tomcat-deployment --type=NodePort
```
3. Descobrindo qual porta foi aberta no cluster para acessar o serviço:
```shell
minikube service tomcat-deployment --url
```

4. Listando todos os pods presente no cluster:
```shell
kubectl get pods
```

5. Adquirindo informações detalhadas sobre determinado pod:
```shell
kubectl describe pod [pod-name]
```

6. Executando comandos nos pods com ***exec*** *(Acessado o shell)*:
```shell
kubectl exec -it [pod-name] bash
```

7. Rodando um pod no cluster a partir de uma imagem qualquer:
```shell
kubectl run my-nginx --image=nginx:1.13 --port=8000
```

8. Deletando o pod criado anteriormente *(deve-se informar o namespace do qual faz parte)*:
```shell
kubectl delete deployment my-nginx --namespace=default
```
