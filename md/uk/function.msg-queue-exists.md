---
navigation:
  - function.msg-get-queue.md: « msggetqueue
  - function.msg-receive.md: msgreceive »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: msgqueueexists
---
# msgqueueexists

(PHP 5> = 5.3.0, PHP 7, PHP 8)

msgqueueexists — Перевірка існування черги повідомлень

### Опис

```methodsynopsis
msg_queue_exists(int $key): bool
```

Перевіряє існування черги повідомлень, що задається ключем `key`

### Список параметрів

`key`

Ключ черги.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [msgremovequeue()](function.msg-remove-queue.md) - Видалення черги повідомлень
-   [msgreceive()](function.msg-receive.md) - Отримання повідомлення з черги повідомлень
-   [msgstatqueue()](function.msg-stat-queue.md) - Отримання інформації із структури даних черги повідомлень
