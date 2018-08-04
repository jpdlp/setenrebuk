#### Maximum reference
kubectl [reference](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands) and [cheat sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

*Conteúdo: verificar a persistência dos dados do wordpress*

---

1. Criando os volumes persistentes a partir do arquivo *.yaml*:
```shell
kubectl create -f local-volumes.yaml
```

2. Exibindo com o ***get*** os volumes persistentes criados:
```shell
kubectl get persistentevolumes
```
