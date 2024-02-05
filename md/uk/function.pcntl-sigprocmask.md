---
navigation:
  - function.pcntl-signal.md: « pcntl\_signal
  - function.pcntl-sigtimedwait.md: pcntl\_sigtimedwait »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntl\_sigprocmask
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pcntl\_sigprocmask

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

pcntl\_sigprocmask — Задає та витягує список сигналів, що блокуються.

### Опис

```methodsynopsis
pcntl_sigprocmask(int $mode, array $signals, array &$old_signals = null): bool
```

Функция**pcntl\_sigprocmask()** додає, видаляє або задає список заблокованих процесів залежно від значення переданого в аргументі `mode`

### Список параметрів

`mode`

Задає поведінку функції **pcntl\_sigprocmask()**. Можливі значення:

-   **`SIG_BLOCK`**: Додати сигнал до списку сигналів, що вже блокуються.
-   **`SIG_UNBLOCK`**: Видалити сигнал зі списку заблокованих.
-   **`SIG_SETMASK`**: Замінити список сигналів, що блокуються, новим списком.

`signals`

Список сигналів

`old_signals`

Функція передасть за посиланням аргумент `old_signals` раніше заданий список сигналів, що блокуються.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**pcntl\_sigprocmask()\*\*\*\*

```php
<?php
pcntl_sigprocmask(SIG_BLOCK, array(SIGHUP));
$oldset = array();
pcntl_sigprocmask(SIG_UNBLOCK, array(SIGHUP), $oldset);
?>
```

### Дивіться також

-   [pcntl\_sigwaitinfo()](function.pcntl-sigwaitinfo.md) \- Очікування сигналів
-   [pcntl\_sigtimedwait()](function.pcntl-sigtimedwait.md) \- Очікує сигнали протягом заданого часу
