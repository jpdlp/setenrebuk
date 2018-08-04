#### Maximum reference
kubectl [reference](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands) and [cheat sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

*Conteúdo: criando uma secret e utilizando-a no arquivo de deployment .yaml*

---

1. Criando uma secret com o ***create secret***:
```shell
kubectl create secret generic mysql-pass --from-literal=password=pass123456
```

2. Criando secret a partir de um arquivo de texto:
```shell
kubectl create secret generic db-user-pass --from-file=./username.txt --from-file=./password.txt
```

3. Exibindo as secrets criadas:
```shell
kubectl get secret
```
