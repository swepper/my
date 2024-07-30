# myapp-ansible

## проект по практике ansible slurm https://edu.slurm.io/courses/devops_upgrade_comfort8/units/6218/lessons/24525/steps/81939

С трудом удалось победить все зависимости и поставить работающие версии пакетов

* nginx как по требованию установлен через galaxy - geerlingguy.nginx
* ruby роль так же ставилась из готовой роли geerlingguy.ruby
* postgres - ручками

Дистрибутив использовался Rocky Linux 8, решил не заниматься некрофильством с 7центосью, но думаю заведется и на 7.9

### установка:
#### развертывание сервера:
vagrant up server_myapp

#### установка приложения:
ansible-playbook playbook.yml

