# 08-ansible-03-yandex
### Этот плейбук работает в окружении `yandex cloud`. Он устанавливает в подготовленные виртуальные машины:
- clickhouse версии "22.3.3.44"
- vector версии "0.29.1"
- [lighthouse](https://github.com/VKCOM/lighthouse)

Для запуска плейбука нобходимо подключить 3 ВМ с образом CentOS-7, в файле `inventory/prod.yml` указать ip-адреса созданных ВМ.

Затем, для запусуа плейбука, можно воспользоватся следующей командой:
```bash
sudo ansible-playbook -i inventory/prod.yml site.yml
``` 
