---
navigation:
  - function.pcntl-sigprocmask.md: « pcntl\_sigprocmask
  - function.pcntl-sigwaitinfo.md: pcntl\_sigwaitinfo »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntl\_sigtimedwait
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pcntl\_sigtimedwait

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

pcntl\_sigtimedwait — Очікує сигнали протягом заданого часу

### Опис

```methodsynopsis
pcntl_sigtimedwait(    array $signals,    array &$info = [],    int $seconds = 0,    int $nanoseconds = 0): int|false
```

Функция**pcntl\_sigtimedwait()** поводиться так само як і функція [pcntl\_sigwaitinfo()](function.pcntl-sigwaitinfo.md) за винятком того, що приймає два додаткові аргументи, `seconds`и`nanoseconds`, які встановлюють верхню межу часу, що скрипт може простоювати.

### Список параметрів

`signals`

Масив очікуваних сигналів.

`info`

`info`содержит информацию о сигнале. Смотрите функцию[pcntl\_sigwaitinfo()](function.pcntl-sigwaitinfo.md)

`seconds`

Час очікування за секунди.

`nanoseconds`

Час очікування у наносекундах.

### Значення, що повертаються

У разі успішного виконання **pcntl\_sigtimedwait()** повертає номер сигналу або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [pcntl\_sigprocmask()](function.pcntl-sigprocmask.md) \- Задає та витягує список сигналів, що блокуються.
-   [pcntl\_sigwaitinfo()](function.pcntl-sigwaitinfo.md) \- Очікування сигналів
