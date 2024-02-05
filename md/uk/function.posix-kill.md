---
navigation:
  - function.posix-isatty.md: « posix\_isatty
  - function.posix-mkfifo.md: posix\_mkfifo »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_kill
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_kill

(PHP 4, PHP 5, PHP 7, PHP 8)

posix\_kill — Надсилає сигнал відповідному процесу

### Опис

```methodsynopsis
posix_kill(int $process_id, int $signal): bool
```

Надсилає сигнал `signal` процесу з ідентифікатором `process_id`

### Список параметрів

`process_id`

Ідентифікатор процесу.

`signal`

Одна из[PCNTL констант сигналів](pcntl.constants.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   kill(2) посібник для POSIX систем, які містять додаткову інформацію про негативні ідентифікатори процесів, спеціальний ідентифікатор 0, спеціальний ідентифікатор -1, і сигнал з ідентифікатором 0.
