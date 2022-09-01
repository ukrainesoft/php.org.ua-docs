---
navigation:
  - function.inotify-init.html: « inotifyinit
  - function.inotify-read.html: inotifyread »
  - index.html: PHP Manual
  - ref.inotify.html: Функции Inotify
title: inotifyqueuelen
---
# inotifyqueuelen

(PECL inotify >= 0.1.2)

inotifyqueuelen — Повертає кількість очікуваних подій у черзі

### Опис

```methodsynopsis
inotify_queue_len(resource $inotify_instance): int
```

Функція дозволяє зрозуміти, чи заблокує [inotifyread()](function.inotify-read.html) виконання чи ні. Якщо повернене число більше нуля, то в черзі є повідомлення та [inotifyread()](function.inotify-read.html) не заблокує виконання скрипту.

### Список параметрів

`inotify_instance`

Ресурс, що повертається [inotifyinit()](function.inotify-init.html)

### Значення, що повертаються

Повертає кількість очікуваних повідомлень у черзі.

### Дивіться також

-   [inotifyinit()](function.inotify-init.html) - Ініціалізує екземпляр inotify
-   [streamselect()](function.stream-select.html) - Запускає еквівалент системного виклику select() на заданих масивах потоків з часом очікування, вказаним параметрами seconds та microseconds
-   [streamsetblocking()](function.stream-set-blocking.html) - Встановити блокуючий/неблокуючий режим у потоці
