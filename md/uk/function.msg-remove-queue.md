---
navigation:
  - function.msg-receive.md: « msgreceive
  - function.msg-send.md: msgsend »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: msgremovequeue
---
# msgremovequeue

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

msgremovequeue — Видалення черги повідомлень

### Опис

```methodsynopsis
msg_remove_queue(SysvMessageQueue $queue): bool
```

**msgremovequeue()** видаляє чергу повідомлень, зазначену у параметрі `queue`. Використовуйте цю функцію тільки тоді, коли всі процеси, що використовували чергу повідомлень, завершили роботу з нею і вам необхідно звільнити системні ресурси.

### Список параметрів

`queue`

Черга повідомлень.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `queue` тепер чекає екземпляр [SysvMessageQueue](class.sysvmessagequeue.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [msggetqueue()](function.msg-get-queue.md) - Створення або підключення до черги повідомлень
-   [msgreceive()](function.msg-receive.md) - Отримання повідомлення з черги повідомлень
-   [msgstatqueue()](function.msg-stat-queue.md) - Отримання інформації із структури даних черги повідомлень
-   [msgsetqueue()](function.msg-set-queue.md) - Встановлення інформації у структурі даних черги повідомлень
