---
navigation:
  - function.pcntl-signal-dispatch.md: « pcntl\_signal\_dispatch
  - function.pcntl-signal.md: pcntl\_signal »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntl\_signal\_get\_handler
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pcntl\_signal\_get\_handler

(PHP 7 >= 7.1.0, PHP 8)

pcntl\_signal\_get\_handler — Отримати поточний обробник вказаного сигналу

### Опис

```methodsynopsis
pcntl_signal_get_handler(int $signal): callable|int
```

Функция**pcntl\_signal\_get\_handler()** отримає поточний обробник вказаного сигналу `signal`

### Список параметрів

`signal`

Номер сигналу.

### Значення, що повертаються

Функція поверне ціле значення, що вказує на константи **`SIG_DFL`**или**`SIG_IGN`**. Якщо заданий обробник користувача, повертається цей [callable](language.types.callable.md). функції.

### список змін

| Версия | Опис |
| --- | --- |
| 7.1.0 | Була додана функція **pcntl\_signal\_get\_handler()** |

### Приклади

**Пример #1 Пример использования**pcntl\_signal\_get\_handler()\*\*\*\*

```php
<?php
var_dump(pcntl_signal_get_handler(SIGUSR1)); // Вывод: int(0)

function pcntl_test($signo) {}
pcntl_signal(SIGUSR1, 'pcntl_test');
var_dump(pcntl_signal_get_handler(SIGUSR1)); // Вывод: string(10) "pcntl_test"

pcntl_signal(SIGUSR1, SIG_DFL);
var_dump(pcntl_signal_get_handler(SIGUSR1)); // Вывод: int(0)

pcntl_signal(SIGUSR1, SIG_IGN);
var_dump(pcntl_signal_get_handler(SIGUSR1)); // Вывод: int(1)
?>
```

### Дивіться також

-   [pcntl\_signal()](function.pcntl-signal.md) \- Встановлення оброблювача сигналу
