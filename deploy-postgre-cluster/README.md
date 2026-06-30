Роль для деплоя кластера:
postgresql
consul
patroni

Схема работы и кто за что отвечает:

Источники:
В качестве consul - https://github.com/ansible-collections/ansible-consul

В качестве patroni - https://github.com/kostiantyn-nemchenko/ansible-role-patroni


В качестве postrgesql - https://github.com/geerlingguy/ansible-role-postgresql

Требования:
- На всех серверах должен быть установлен openssh-server
 - На всех серверах echo 'ubuntu ALL=(ALL) NOPASSWD:ALL' | sudo tee /etc/sudoers.d/ubuntu-nopasswd

