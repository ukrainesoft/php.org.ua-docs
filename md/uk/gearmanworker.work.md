---
navigation:
  - gearmanworker.wait.md: '« GearmanWorker::wait'
  - class.gearmanexception.md: GearmanException »
  - index.md: PHP Manual
  - class.gearmanworker.md: GearmanWorker
title: 'GearmanWorker::work'
---
# GearmanWorker::work

(PECL gearman >= 0.5.0)

GearmanWorker::work — Очікування та виконання завдань

### Опис

```methodsynopsis
public GearmanWorker::work(): bool
```

Чекає від сервера завдання, а потім викликає відповідну callback-функцію для обробки. Викликає помилку рівня **`E_WARNING`** з інформацією про останню помилку Gearman у випадках, коли код повернення функції відрізняється від **`GEARMAN_SUCCESS`** **`GEARMAN_IO_WAIT`** або **`GEARMAN_WORK_FAIL`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **GearmanWorker::work()****

```php
<?php

# создаём обработчик
$worker = new GearmanWorker();

# добавляем сервер заданий по умолчанию (localhost)
$worker->addServer();

# добавляем callback-функцию
$worker->addFunction("reverse", "my_reverse_function");

# запускаем обработчик, ожидающий заданий от сервера
while ($worker->work());

function my_reverse_function($job)
{
  return strrev($job->workload());
}

?>
```

### Дивіться також

-   [GearmanWorker::addFunction()](gearmanworker.addfunction.md) - Реєстрація та додавання callback-функції
