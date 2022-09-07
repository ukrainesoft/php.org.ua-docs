---
navigation:
  - gearmanworker.addoptions.md: '« GearmanWorker::addOptions'
  - gearmanworker.addservers.md: 'GearmanWorker::addServers »'
  - index.md: PHP Manual
  - class.gearmanworker.md: GearmanWorker
title: 'GearmanWorker::addServer'
---
# GearmanWorker::addServer

(PECL gearman >= 0.5.0)

GearmanWorker::addServer — Додавання сервера завдань

### Опис

```methodsynopsis
public GearmanWorker::addServer(string $host = 127.0.0.1, int $port = 4730): bool
```

Додає сервер завдань до оброблювача. Обробник зберігає список серверів, від яких може отримувати завдання на обробку. Метод просто додає інформацію про сервер до цього списку, ніякого обміну даними між сервером і обробником в цей момент не відбувається.

### Список параметрів

`host`

Ім'я сервера хоста завдань.

`port`

Порт сервера завдань.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Додавання альтернативних серверів Gearman**

```php
<?php
$worker= new GearmanWorker();
$worker->addServer("10.0.0.1");
$worker->addServer("10.0.0.2", 7003);
?>
```

### Дивіться також

-   [GearmanWorker::addServers()](gearmanworker.addservers.md) - Додавання серверів завдань
