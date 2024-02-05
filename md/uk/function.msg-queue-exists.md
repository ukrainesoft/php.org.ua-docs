---
navigation:
  - function.msg-get-queue.md: « msg\_get\_queue
  - function.msg-receive.md: msg\_receive »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: msg\_queue\_exists
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# msg\_queue\_exists

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

msg\_queue\_exists — Перевірка існування черги повідомлень

### Опис

```methodsynopsis
msg_queue_exists(int $key): bool
```

Проверяет существование очереди сообщений, задаваемой ключом`key`

### Список параметрів

`key`

Ключ черги.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [msg\_remove\_queue()](function.msg-remove-queue.md) \- Видалення черги повідомлень
-   [msg\_receive()](function.msg-receive.md) \- Отримання повідомлення з черги повідомлень
-   [msg\_stat\_queue()](function.msg-stat-queue.md) \- Отримання інформації із структури даних черги повідомлень
