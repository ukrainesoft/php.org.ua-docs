---
navigation:
  - gearmanclient.addoptions.md: '« GearmanClient::addOptions'
  - gearmanclient.addservers.md: 'GearmanClient::addServers »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::addServer'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanClient::addServer

(PECL gearman >= 0.5.0)

GearmanClient::addServer — Додати сервер завдань для клієнта

### Опис

```methodsynopsis
public GearmanClient::addServer(string $host = null, int $port = 0, bool $setupExceptionHandler = true): bool
```

Додає сервер завдань до списку серверів, які можуть бути використані для виконання завдання. Жодних операцій введення-виведення з сокетом тут не відбувається. Сервер просто додається до списку.

### Список параметрів

`host`

Ім'я сервера хоста завдань.

`port`

Порт сервера завдань.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Додавання двох серверів завдань**

```php
<?php

# Создаём клиентский объект
$gmclient= new GearmanClient();

# Добавляем два сервера задач, первый из них работает по умолчанию на порту 4730
$gmclient->addServer("10.0.0.1");
$gmclient->addServer("10.0.0.2", 7003);

?>
```

### Дивіться також

-   [GearmanClient::addServers()](gearmanclient.addservers.md) \- Додати список серверів завдань для клієнта
