#### Maximum reference
kubectl [reference](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands), [cheat sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/) and [labels & selectors](https://kubernetes.io/docs/concepts/overview/working-with-objects/labels/)

---

#### Comandos de label

1. Adicionando um *label* ao node *(minikube)*:
```shell
kubectl label node minikube storageType=ssd
```

2. Verificando a aplicação do *label*:
```shell
kubectl describe node minikube
```
