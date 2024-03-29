---
navigation:
  - gearmanworker.addserver.md: '« GearmanWorker::addServer'
  - gearmanworker.clone.md: 'GearmanWorker::clone »'
  - index.md: PHP Manual
  - class.gearmanworker.md: GearmanWorker
title: 'GearmanWorker::addServers'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanWorker::addServers

(PECL gearman >= 0.5.0)

GearmanWorker::addServers — Додавання серверів завдань

### Опис

```methodsynopsis
public GearmanWorker::addServers(string $servers = null, bool $setupExceptionHandler = true): bool
```

Додає один або кілька серверів завдань у цей обробник. Обробник зберігає список серверів, від яких може отримувати завдання на обробку. Метод просто додає інформацію про сервери до цього списку, жодного обміну даними між сервером та обробником у цей момент не відбувається.

### Список параметрів

`servers`

Список розділених комів серверів у форматі хост:порт. Якщо порт не вказано, за промовчанням приймається номер 4730.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Додавання двох серверів завдань**

```php
<?php

$worker= new GearmanWorker();
$worker->addServers("10.0.0.1,10.0.0.2:7003");

?>
```

### Дивіться також

-   [GearmanWorker::addServer()](gearmanworker.addserver.md) \- Додавання сервера завдань
