### Cenário prático
#### *Namespace & Resource Quotas*

---
**Etapas**:

1. Criar um namespace

2. Atribuir-lhe um limite de 400m (40%) de CPU

3. Criar um deployment *(tomcat)* com 3 réplicas nesse novo namespace. Cada réplica terá 200m (20%) de CPU.

4. Usar o kubectl para examinar o status do deployment


**Obs**: O intuito desse cenário é observar como o kubernetes lida com a violação do limite de uma quota.
