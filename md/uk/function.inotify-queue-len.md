---
navigation:
  - function.inotify-init.md: « inotify\_init
  - function.inotify-read.md: inotify\_read »
  - index.md: PHP Manual
  - ref.inotify.md: Функції Inotify
title: inotify\_queue\_len
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# inotify\_queue\_len

(PECL inotify >= 0.1.2)

inotify\_queue\_len — Повертає кількість очікуваних подій у черзі

### Опис

```methodsynopsis
inotify_queue_len(resource $inotify_instance): int
```

Функція дозволяє зрозуміти, чи заблокує [inotify\_read()](function.inotify-read.md) виконання чи ні. Якщо повернене число більше нуля, то в черзі є повідомлення та [inotify\_read()](function.inotify-read.md) не заблокує виконання скрипту.

### Список параметрів

`inotify_instance`

Ресурс, що повертається [inotify\_init()](function.inotify-init.md)

### Значення, що повертаються

Повертає кількість очікуваних повідомлень у черзі.

### Дивіться також

-   [inotify\_init()](function.inotify-init.md) \- Ініціалізує екземпляр inotify
-   [stream\_select()](function.stream-select.md) \- Запускає еквівалент системного виклику select() на заданих масивах потоків з часом очікування, вказаним параметрами seconds та microseconds
-   [stream\_set\_blocking()](function.stream-set-blocking.md) \- Встановити блокуючий/неблокуючий режим у потоці
