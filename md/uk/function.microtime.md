---
navigation:
  - function.localtime.md: « localtime
  - function.mktime.md: mktime »
  - index.md: PHP Manual
  - ref.datetime.md: Функції дати та часу
title: microtime
---
# microtime

(PHP 4, PHP 5, PHP 7, PHP 8)

microtime — Повертає поточну позначку часу Unix з мікросекундами

### Опис

```methodsynopsis
microtime(bool $as_float = false): string|float
```

Функція **microtime()** повертає поточну позначку часу Unix з мікросекундами. Ця функція доступна лише на операційних системах, у яких є системний виклик gettimeofday().

Для вимірювання продуктивності рекомендується використовувати [hrtime()](function.hrtime.md)

### Список параметрів

`as_float`

Якщо вказано та встановлено в **`true`** **microtime()** поверне число з плаваючою точкою (float) замість рядка (string), як описано в розділі значень, що повертаються нижче.

### Значення, що повертаються

За замовчуванням **microtime()** повертає рядок (string) у форматі "msec sec", де `sec` являє собою кількість секунд з початку епохи Unix (1 січня 1970 0:00:00 GMT), а `msec` - це кількість мікросекунд, що пройшли після `sec`

Якщо параметр `as_float` встановлений в **`true`**, то **microtime()** поверне результат у речовинному вигляді (float), що є поточний час у секундах, що пройшли з початку епохи Unix з точністю до мікросекунд.

### Приклади

**Приклад #1 Вимірювання часу виконання скрипту**

```php
<?php
$time_start = microtime(true);

// Спим некоторое время
usleep(100);

$time_end = microtime(true);
$time = $time_end - $time_start;

echo "Ничего не делал $time секунд\n";
?>
```

**Приклад #2 Приклад використання **microtime()** і `REQUEST_TIME_FLOAT`**

```php
<?php
// Выбираем время сна случайным образом
usleep(mt_rand(100, 10000));

// В суперглобальном Масиве $_SERVER доступно значение REQUEST_TIME_FLOAT.
// Оно содержит временную метку начала запроса с точностью до микросекунд.
$time = microtime(true) - $_SERVER["REQUEST_TIME_FLOAT"];

echo "Ничего не делал $time секунд\n";
?>
```

### Дивіться також

-   [time()](function.time.md) - Повертає поточну мітку системного часу Unix
-   [hrtime()](function.hrtime.md) - Отримати системний час високого дозволу
