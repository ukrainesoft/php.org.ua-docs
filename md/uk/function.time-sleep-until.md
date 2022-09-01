---
navigation:
  - function.time-nanosleep.html: « timenanosleep
  - function.uniqid.md: uniqid »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: timesleepuntil
---
# timesleepuntil

(PHP 5> = 5.1.0, PHP 7, PHP 8)

timesleepuntil - Відкладає виконання скрипту до заданого часу

### Опис

```methodsynopsis
time_sleep_until(float $timestamp): bool
```

Відкладає виконання скрипту до заданої часової мітки, вказаної у параметрі `timestamp`

### Список параметрів

`timestamp`

Тимчасова мітка продовження виконання скрипту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Якщо вказана тимчасова мітка `timestamp` прострочена, то функція згенерує **`E_WARNING`**

### Приклади

**Приклад #1 Приклад використання **timesleepuntil()****

```php
<?php

//возвращает false и выводит предупреждение
var_dump(time_sleep_until(time()-1));

// может работать только на быстродействующих компьютерах, выполнение отложено до 0.2 секунд
var_dump(time_sleep_until(microtime(true)+0.2));

?>
```

### Примітки

> **Зауваження**: Усі сигнали будуть доставлені після виконання скрипту.

### Дивіться також

-   [sleep()](function.sleep.md) - затримка виконання
-   [usleep()](function.usleep.md) - Затримка виконання у мікросекундах
-   [timenanosleep()](function.time-nanosleep.md) - Затримка на задану кількість секунд та наносекунд
-   [settimelimit()](function.set-time-limit.md) - Обмеження часу виконання скрипту
