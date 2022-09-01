---
navigation:
  - gearmanclient.addserver.html: '« GearmanClient::addServer'
  - gearmanclient.addtask.html: 'GearmanClient::addTask »'
  - index.html: PHP Manual
  - class.gearmanclient.html: GearmanClient
title: 'GearmanClient::addServers'
---
# GearmanClient::addServers

(PECL gearman >= 0.5.0)

GearmanClient::addServers — Додати список серверів завдань для клієнта

### Опис

```methodsynopsis
public GearmanClient::addServers(string $servers = 127.0.0.1:4730): bool
```

Додає список серверів завдань, які можуть бути використані для виконання завдання. Жодних операцій введення-виведення з сокетом тут не відбувається. Сервери просто додаються до повного списку серверів.

### Список параметрів

`servers`

Список серверів, розділених комами. Кожен сервер вказано у форматі '`host:port`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Додавання двох серверів завдань**

```php
<?php

# Создаём наш клиентский объект
$gmclient= new GearmanClient();

# Добавляем несколько серверов задач, первый из них работает по умолчанию на порту 4730
$gmclient->addServers("10.0.0.1,10.0.0.2:7003");

?>
```

### Дивіться також

-   [GearmanClient::addServer()](gearmanclient.addserver.md) - Додати сервер завдань для клієнта
