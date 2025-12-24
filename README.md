# Плейбук для установки OpenVPN сервера
Поддерживаемая ОС: Ubuntu (22.04, 24.04)

Предварительно нужно переделать инвентарь под себя или заменить в нем значения на переменные, чтобы потом передавать их через extra-vars 

Пример команды запуска:
```shell
 ansible-playbook main.yml --extra-vars='{
"vpn-server-1_host":"127.0.0.1",
"vpn-server-1_user":"ubuntu",
"vpn-server-1_ip":"127.0.0.1",
"vpn-server-1_name":"server",
"client_1_name":"client_1",
"client_2_name":"client_2"
 }' -i inventory.yml
```

Если нужно сгенерировать новый клиентский сертефикат, достаточно запустить плейбук `generate-client.yml`