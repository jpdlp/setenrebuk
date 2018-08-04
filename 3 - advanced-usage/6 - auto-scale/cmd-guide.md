#### Maximum reference
kubectl [reference](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands) and [cheat sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

*Auto scalling com o HPA - Horizontal Pod Autoscaler*

---

1. Aplicando o novo *deployment* com limitação de CPU do wordpress.
```shell
kubectl apply -f ./wordpress-deployment.yaml
```

2. Configurando o HPA *auto scale* no wordpress para escalonar novos pods *(maximo de 5)* caso a utilização de cpu do conjunto ultrapasse 50%.
```shell
kubectl autoscale deployment wordpress --cpu-percent=50 --min=1 —max=5
```

3. Criando um novo pod (load-generator) que irar gerar infinitas requisições no wordpress
```shell
kubectl run -i --tty load-generator --image=busybox /bin/sh
$ while true; do wget -q -O- http://wordpress.default.svc.cluster.local; done
```

4. Checando o status do HPA.
```shell
kubectl get hpa
```
