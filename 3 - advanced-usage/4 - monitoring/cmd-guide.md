#### Maximum reference
kubectl [reference](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands) and [cheat sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

*Resource monitoring*

---
1. O kubernetes possui "nativamente" algumas ferramentas open sources para a Monitoração de Recursos e Uso. São elas:

  - [Heapster](https://github.com/kubernetes/heapster)

  - [InfluxDB](https://docs.influxdata.com/influxdb/v1.6/)

  - [Grafana](http://docs.grafana.org/)

2. No minikube *(cluster local)* essas ferramentas devem ser habilidatas. Para habilitar:
```shell
minikube addons enable heapster
```

3. Checando o status dos pods *influx* e *Heapster*:
```shell
kubectl get pods --namespace=kube-system
```

4. Acessando a Dashboard do *Grafana*:
```shell
minikube addons open heapster
```
