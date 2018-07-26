#### Maximum reference
kubectl [reference](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands) and [cheat sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

---

#### Comandos de deploy

1. Listando os deployments:
```shell
kubectl get deployments
```

2. Checando os rollouts dos deployments:
```shell
kubectl rollout deployment tomcat-deployment
```

3. Modificando a imagem do deployment com o ***set***:
```shell
kubectl set image deployment/tomcat-deployment tomcat=tomcat:9.0.1
```

4. Verificando o histórica dos rollouts:
```shell
kubectl rollout history deployment/tomcat-deployment
```
