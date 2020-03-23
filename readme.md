# MikroTik.

## Сброс
Сбрасываем конфигурацию в ноль. <br>
```
System => Reset Configuration => [V]No Default Configuration => [Reset Configuration] => [Yes]
```
![](./img/ResetConf.png)<br>
## Cетевой мост (bridge).
Создаем сетевой мост по умолчанию. <br>
```
Bridge => Bridge => [+] => [OK]
```
![](./img/Bridge_Bridge.png)<br>
Добавляем в него все локальные интерфейсы.<br>
```
Bridge => Ports => General => Interface: <interface> => [OK]
```
![](./img/Bridge_Ports.png)<br>

## DHCP Server.
Проверяем что у нас есть IP-адрес на интерфейсе с которого мы собираемся слушать дисковер запросы(раздавать адреса).<br>
```
IP => Addresses
```
![](./img/IP_Address(DHCP).png)<br>

Создаём пул адресов для DHCP. <br>
```
IP => Pool => Pools => [+]
```
![](./img/IP_Pool_Pools_DHCP.png)<br>

Задаём основные настройки сети.

```
IP => DHCP Server => [DHCP] => Networks => [+]
```

![](./img/IP_DHCP-Server_Networks.png)<br>

Создаем DHCP Server.

```
#IP => DHCP Server => [DHCP] => [+]
```

![](./img/IP_DHCP-Server_DHCP.png)<br>

#### Fork + Git
    1. создаём локальную папку репозитория. (не забываем про General settings).
    2. Fork, инициализируем локальный репозиторий(из пункта 1).
    3. создаём внешний репозиторий(git).
    4. Fork, инициализируем внешний репозиторий(из пункта 3).
    5. создаём 'readme.md'
    6. создаём коммит 'init: master' и пушим изменения.(master ветка создана локално и origin).
    7. инициализируем 'git flow'.
    8. переходим в ветку 'develop'.
    9. пишем название проекта(или что угодно) в 'readme.md'.
    10. создаём коммит 'init: develop' и пушим изменения.(develop ветка создана локално и origin).
    11. создаём ветку 'feature/govnokod', и начинаем творить(по возможности пишем: локоничные 'коммиты' и исчерпывающие 'дискрипшены').