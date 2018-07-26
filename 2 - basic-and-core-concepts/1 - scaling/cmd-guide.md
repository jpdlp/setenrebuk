#### Maximum reference
kubectl [reference](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands) and [cheat sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

---

#### Comandos de escalonamento

1. Criando/adicionando réplicas de um deploy existente com o ***scale***:
```
kubectl scale --replicas=4 deployment/tomcat-deployment
```

2. Expondo as portas das replicas criadas *(criando um load balancer)*:
```
kubectl expose deployment tomcat-deployment --type=LoadBalancer --port=8080 --target-port=8080 --name=tomcat-load-balancer
```

3. Obtendo detalhes do novo serviço *load balancer*:
```
kubectl describe services tomcat-load-balancer
```
