---
navigation:
  - function.msg-receive.md: « msg\_receive
  - function.msg-send.md: msg\_send »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: msg\_remove\_queue
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# msg\_remove\_queue

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

msg\_remove\_queue — Видалення черги повідомлень

### Опис

```methodsynopsis
msg_remove_queue(SysvMessageQueue $queue): bool
```

**msg\_remove\_queue()** видаляє чергу повідомлень, зазначену у параметрі `queue`. Використовуйте цю функцію тільки тоді, коли всі процеси, що використовували чергу повідомлень, завершили роботу з нею і вам необхідно звільнити системні ресурси.

### Список параметрів

`queue`

Черга повідомлень.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`queue` тепер чекає екземпляр [SysvMessageQueue](class.sysvmessagequeue.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [msg\_get\_queue()](function.msg-get-queue.md) \- Створення або підключення до черги повідомлень
-   [msg\_receive()](function.msg-receive.md) \- Отримання повідомлення з черги повідомлень
-   [msg\_stat\_queue()](function.msg-stat-queue.md) \- Отримання інформації із структури даних черги повідомлень
-   [msg\_set\_queue()](function.msg-set-queue.md) \- Встановлення інформації у структурі даних черги повідомлень
