#### Criando um deployment do mongoDB com 4 réplicas
*Outra alternativa ao método de aplicar as configurações descritas no arquivo .yaml*

---

1. Criando um deploy específico do mongo *(3.4)* com o *kubectl run*:
```shell
kubectl run mongo-deployment --image=mongo:3.4-jessie --port=27017
```

2. Criando as 4 réplicas com o *kubectl scale*:
```shell
kubectl scale --replicas=4 deployment/mongo-deployment
```
