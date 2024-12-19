# Update Kubernetes Version

Este playbook tem como objetivo fazer atualização de versões do Kubernetes.\
Ele atualiza o repositório, control planes e workers.

## Como utilizar

Defina os hosts no arquivo de inventário <hosts.cfg>.\
Tenha ssh_key dos hosts para acesso.

Defina as variáveis de versão em <vars.yaml>.

Execute:
```
ansible-playbook -i hosts.cfg playbook.yaml --extra-vars "@vars.yaml" -b -K 
```