---
navigation:
  - function.pcntl-signal-dispatch.html: pcntlsignaldispatch
  - function.pcntl-signal.html: pcntlsignal »
  - index.html: PHP Manual
  - ref.pcntl.html: Функції PCNTL
title: pcntlsignalgethandler
---
# pcntlsignalgethandler

(PHP 7> = 7.1.0, PHP 8)

pcntlsignalgethandler — Отримати поточний обробник вказаного сигналу

### Опис

```methodsynopsis
pcntl_signal_get_handler(int $signal): callable|int
```

Функція **pcntlsignalgethandler()** отримає поточний обробник вказаного сигналу `signal`

### Список параметрів

`signal`

Номер сигналу.

### Значення, що повертаються

Функція поверне ціле значення, що вказує на константи **`SIG_DFL`** або **`SIG_IGN`**. Якщо заданий обробник користувача, повертається цей [callable](language.types.callable.html). функції.

### список змін

| Версия | Описание |
| --- | --- |
|  | Була додана функція **pcntlsignalgethandler()** |

### Приклади

**Приклад #1 Приклад використання **pcntlsignalgethandler()****

```php
<?php
var_dump(pcntl_signal_get_handler(SIGUSR1)); // Вывод: int(0)

function pcntl_test($signo) {}
pcntl_signal(SIGUSR1, 'pcntl_test');
var_dump(pcntl_signal_get_handler(SIGUSR1)); // Вывод: string(10) "pcntl_test"

pcntl_signal(SIGUSR1, SIG_DFL);
var_dump(pcntl_signal_get_handler(SIGUSR1)); // Вывод: int(0)

pcntl_signal(SIGUSR1, SIG_IGN);
var_dump(pcntl_signal_get_handler(SIGUSR1)); // Вывод: int(1)
?>
```

### Дивіться також

-   [pcntlsignal()](function.pcntl-signal.html) - Встановлення оброблювача сигналу
