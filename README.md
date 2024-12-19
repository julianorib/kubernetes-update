# Update Kubernetes Version

Este playbook tem como objetivo fazer atualização de versão do Kubernetes.\
Ele atualiza o repositório, control planes e workers. 

*Observação: Kubernetes instalado em Derivadados do Redhat.*

A atualização é feita um (1) host de cada vez.

## Como utilizar

Defina os hosts no arquivo de inventário <hosts.cfg>.\
Tenha ssh_key dos hosts para acesso.

Defina as variáveis de versão em <vars.yaml>.

<https://kubernetes.io/releases/>

- repo
- reponew
- version

Execute:
```
ansible-playbook -i hosts.cfg playbook.yaml --extra-vars "@vars.yaml" -b -K 
```

## Melhorias pendentes

- Modificar tasks de repositório incluindo opção de Derivados Debian.
- Modificar tasks de atualização de pacotes com condicionais de S.O.