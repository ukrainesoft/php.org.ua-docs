---
navigation:
  - function.inotify-init.md: « inotifyinit
  - function.inotify-read.md: inotifyread »
  - index.md: PHP Manual
  - ref.inotify.md: Функции Inotify
title: inotifyqueuelen
---
# inotifyqueuelen

(PECL inotify >= 0.1.2)

inotifyqueuelen — Повертає кількість очікуваних подій у черзі

### Опис

```methodsynopsis
inotify_queue_len(resource $inotify_instance): int
```

Функція дозволяє зрозуміти, чи заблокує [inotifyread()](function.inotify-read.md) виконання чи ні. Якщо повернене число більше нуля, то в черзі є повідомлення та [inotifyread()](function.inotify-read.md) не заблокує виконання скрипту.

### Список параметрів

`inotify_instance`

Ресурс, що повертається [inotifyinit()](function.inotify-init.md)

### Значення, що повертаються

Повертає кількість очікуваних повідомлень у черзі.

### Дивіться також

-   [inotifyinit()](function.inotify-init.md) - Ініціалізує екземпляр inotify
-   [streamselect()](function.stream-select.md) - Запускає еквівалент системного виклику select() на заданих масивах потоків з часом очікування, вказаним параметрами seconds та microseconds
-   [streamsetblocking()](function.stream-set-blocking.md) - Встановити блокуючий/неблокуючий режим у потоці
