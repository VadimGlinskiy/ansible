Роль для деплоя кластера:
postgresql
consul
patroni

Схема работы и кто за что отвечает:

Consul - Ставится первым на все ноды, в данном случае на все три ноды, образуя кворум;
Consul регулирует, кто является мастером, с помощью особо механизма блокировки, и затем какое-либо приложение опрашивает Consul и по ключ:значение определяет, кто сейчас лидер, если лидер упал, задействуется механизм по выбору нового лидера

Источники:
В качестве consul - https://github.com/ansible-collections/ansible-consul

В качестве patroni - https://github.com/kostiantyn-nemchenko/ansible-role-patroni


В качестве postrgesql - https://github.com/geerlingguy/ansible-role-postgresql

Требования:
- На всех серверах должен быть установлен openssh-server
- На всех серверах echo 'ubuntu ALL=(ALL) NOPASSWD:ALL' | sudo tee /etc/sudoers.d/ubuntu-nopasswd
- Локально у себя
    sudo apt update
    sudo apt install python3-virtualenv -y
    Включенный ВПН
