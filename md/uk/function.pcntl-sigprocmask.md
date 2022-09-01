---
navigation:
  - function.pcntl-signal.html: pcntlsignal
  - function.pcntl-sigtimedwait.html: pcntlsigtimedwait »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntlsigprocmask
---
# pcntlsigprocmask

(PHP 5> = 5.3.0, PHP 7, PHP 8)

pcntlsigprocmask — Задає та витягує список сигналів, що блокуються.

### Опис

```methodsynopsis
pcntl_sigprocmask(int $mode, array $signals, array &$old_signals = null): bool
```

Функція **pcntlsigprocmask()** додає, видаляє або задає список заблокованих процесів залежно від значення переданого в аргументі `mode`

### Список параметрів

`mode`

Задає поведінку функції **pcntlsigprocmask()**. Можливі значення:

-   **`SIG_BLOCK`**: Додати сигнал до списку сигналів, що вже блокуються.
-   **`SIG_UNBLOCK`**: Видалити сигнал зі списку заблокованих.
-   **`SIG_SETMASK`**: Замінити список сигналів, що блокуються, новим списком.

`signals`

Список сигналів

`old_signals`

Функція передасть за посиланням аргумент `old_signals` раніше заданий список сигналів, що блокуються.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **pcntlsigprocmask()****

```php
<?php
pcntl_sigprocmask(SIG_BLOCK, array(SIGHUP));
$oldset = array();
pcntl_sigprocmask(SIG_UNBLOCK, array(SIGHUP), $oldset);
?>
```

### Дивіться також

-   [pcntlsigwaitinfo()](function.pcntl-sigwaitinfo.md) - Очікування сигналів
-   [pcntlsigtimedwait()](function.pcntl-sigtimedwait.md) - Очікує сигнали протягом заданого часу
