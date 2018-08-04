#### Maximum reference
kubectl [reference](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands) and [cheat sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

*Namespaces & Quotas: baseado no cenário prático*

---

1. Criando um *namespace* chamado cpu-limited-tomcat
```shell
kubectl create namespace cpu-limited-tomcat
```

2. Listando todos os *namespaces*:
```shell
kubectl get namespaces
```

3. Atribuindo um limite ao *namespace* recém criado através de um arquivo *.yaml*:
```shell
kubectl create -f cpu-limits.yaml --namespace=cpu-limited-tomcat
```

4. Verificando se a quota foi aplicada e verificando a sua configuração:
```shell
kubectl get resourcequotas --namespace=cpu-limited-tomcat
kubectl describe resourcequotas --namespace=cpu-limited-tomcat
```

5. Criando o *deployment* tomcat no *namespace* criado. **Obs**: se nenhum *namespace* for declarado, o *deployment* será criado no *namespace* default.
```shell
kubectl apply -f ./tomcat-deployment.yaml --namespace=cpu-limited-tomcat
```

6. Obtendo informações sobre o deployment criado:
```
kubectl describe deployment tomcat-deployment --namespace=cpu-limited-tomcat
```
