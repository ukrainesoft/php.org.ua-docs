Додати сервер завдань для клієнта

-   [« GearmanClient::addOptions](gearmanclient.addoptions.html)
    
-   [GearmanClient::addServers »](gearmanclient.addservers.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanClient](class.gearmanclient.html)
    
-   Додати сервер завдань для клієнта
    

# GearmanClient::addServer

(PECL gearman >= 0.5.0)

GearmanClient::addServer — Додати сервер завдань для клієнта

### Опис

```methodsynopsis
public GearmanClient::addServer(string $host = 127.0.0.1, int $port = 4730): bool
```

Додає сервер завдань до списку серверів, які можуть бути використані для виконання завдання. Жодних операцій введення-виведення з сокетом тут не відбувається. Сервер просто додається до списку.

### Список параметрів

`host`

Ім'я сервера хоста завдань.

`port`

Порт сервера завдань.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Додавання двох серверів завдань**

```php
<?php

# Создаём клиентский объект
$gmclient= new GearmanClient();

# Добавляем два сервера задач, первый из них работает по умолчанию на порту 4730
$gmclient->addServer("10.0.0.1");
$gmclient->addServer("10.0.0.2", 7003);

?>
```

### Дивіться також

-   [GearmanClient::addServers()](gearmanclient.addservers.html) - Додати список серверів завдань для клієнта