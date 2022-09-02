---
navigation:
  - class.gearmanworker.md: « GearmanWorker
  - gearmanworker.addoptions.md: 'GearmanWorker::addOptions »'
  - index.md: PHP Manual
  - class.gearmanworker.md: GearmanWorker
title: 'GearmanWorker::addFunction'
---
# GearmanWorker::addFunction

(PECL gearman >= 0.5.0)

GearmanWorker::addFunction — Реєстрація та додавання callback-функції

### Опис

```methodsynopsis
public GearmanWorker::addFunction(    string $function_name,    callable $function,    mixed &$context = ?,    int $timeout = ?): bool
```

Реєструє ім'я функції на сервері завдань і додає посилання на цю функцію зворотного дзвінка. Необов'язково можна задати додаткові дані контексту, які використовуватимуться під час виклику callback-функції та час очікування.

### Список параметрів

`function_name`

Ім'я функції, яку потрібно зареєструвати на сервері завдань.

`function`

Callback-функція, яка буде викликатись, коли сервер отримає завдання для зареєстрованого імені.

`context`

Посилання на довільні дані контексту програми, до яких потрібно забезпечити доступ із функції.

`timeout`

Часовий інтервал у секундах

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Простий обробник використовує додаткові дані контексту програми**

```php
<?php

# получаем обработчик gearman
$worker= new GearmanWorker();

# добавляем сервер по умолчанию (localhost)
$worker->addServer();

# определяем переменную, в которой будут храниться данные приложения
$count= 0;

# добавляем функцию "reverse"
$worker->addFunction("reverse", "reverse_cb", $count);

# запускаем обработчик
while ($worker->work());

function reverse_cb($job, &$count)
{
  $count++;
  return "$count: " . strrev($job->workload());
}

?>
```

Якщо клієнт надішле два завдання для функції reverse, то висновок буде наступним:

```
1: olleh
2: dlrow
```

### Дивіться також

-   [GearmanClient::do()](gearmanclient.do.md) - Виконує одне завдання та повертає результат Застарілий метод
