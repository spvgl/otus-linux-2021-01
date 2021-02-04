# HW02 -- Работа с mdadm

* Методичка по ДЗ -- в ЛК.
* Изначальный `Vagrantfile` -- https://github.com/erlong15/otus-linux/blob/master/Vagrantfile

## 1. Косметические изменения в исходном Vagrantfile

* Имя VM: `otuslinux` -> `hw02-mdadm`
* Добавил в `MACHINES` (и соответствующим образом изменил раздел с созданием VM) следующее:
```
:vm_name => "hw02-mdadm__otus-linux-spv",
:cpus => 1,
:memory => 1024,
```
* Убрал установку `ip_addr`
* Диски создаются в папке VM, а не в текущей.
* Контроллер для диска создается перед созданием дисков, а диски добавляются в контроллер при их создании, а не позже.