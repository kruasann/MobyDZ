### PolKit 
Необходимо создать правило которое:
* Разрешит изменение Network Manager только для root пользователя [43-50 строчка](Vagrantfile)
* Предоставит обычному пользователю права на обновление системы и установку/удаление программ [53-63 строчка](Vagrantfile)
### ACL
* Необходимо запретить группе user делать что угодно с любым ранее созданным файлом. [66-87 строчка](Vagrantfile)

### iptables
* Разрешить входящие соединения с localhost [90 строчка](Vagrantfile)
* Разрешить SSH / Запретить HTTP - порт [91-92 строчка](Vagrantfile)
* Разрешить машинам локальной сети ходить в интернет по указанным TCP портам (10.210.19.0/24, порт 443 и 8080) [93-94 строчка](Vagrantfile)
* Включить NAT для локальной подсети, предположим, что у нас нет статики и настроим [95 строчка](Vagrantfile)

### chroot
1. Создайте и настройте chroot окружение для тестирования веб-приложения на nginx. [101-107 строчка](Vagrantfile)
* debootstrap

2. Установите необходимые пакеты внутри chroot. [110 строчка](Vagrantfile)

3. Протестируйте веб-приложение внутри chroot окружения.
* Запустите веб-сервер nginx внутри chroot. [113 строчка](Vagrantfile)
* Проверьте доступность веб-приложения, используя curl или браузер извне chroot окружения. [116 строчка](Vagrantfile)
