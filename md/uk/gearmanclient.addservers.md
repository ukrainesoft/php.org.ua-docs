---
navigation:
  - gearmanclient.addserver.md: '« GearmanClient::addServer'
  - gearmanclient.addtask.md: 'GearmanClient::addTask »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::addServers'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanClient::addServers

(PECL gearman >= 0.5.0)

GearmanClient::addServers — Додати список серверів завдань для клієнта

### Опис

```methodsynopsis
public GearmanClient::addServers(string $servers = null, bool $setupExceptionHandler = true): bool
```

Додає список серверів завдань, які можуть бути використані для виконання завдання. Жодних операцій введення-виведення з сокетом тут не відбувається. Сервери просто додаються до повного списку серверів.

### Список параметрів

`servers`

Список серверів, розділених комами. Кожен сервер вказано у форматі '`host:port`'.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Додавання двох серверів завдань**

```php
<?php

# Создаём наш клиентский объект
$gmclient= new GearmanClient();

# Добавляем несколько серверов задач, первый из них работает по умолчанию на порту 4730
$gmclient->addServers("10.0.0.1,10.0.0.2:7003");

?>
```

### Дивіться також

-   [GearmanClient::addServer()](gearmanclient.addserver.md) \- Додати сервер завдань для клієнта
