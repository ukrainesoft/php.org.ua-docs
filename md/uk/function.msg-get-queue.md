---
navigation:
  - function.ftok.md: « ftok
  - function.msg-queue-exists.md: msg\_queue\_exists »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: msg\_get\_queue
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# msg\_get\_queue

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

msg\_get\_queue — Створення або підключення до черги повідомлень

### Опис

```methodsynopsis
msg_get_queue(int $key, int $permissions = 0666): SysvMessageQueue|false
```

**msg\_get\_queue()** повертає ідентифікатор, який використовується для доступу до черги повідомлень System V із зазначеним ключем `key`. Перший виклик створює чергу повідомлень із необов'язковими правами `permissions`. Другий та наступні виклики **msg\_get\_queue()** для того ж `key` повертатимуть інші ідентифікатори, проте всі вони посилатимуться на ту саму чергу повідомлень.

### Список параметрів

`key`

Числовий ідентифікатор черги повідомлень.

`permissions`

Права доступа к очереди. По умолчанию 0666. Если очередь сообщений уже существует, параметр`permissions` ігнорується.

### Значення, що повертаються

Повертає екземпляр [SysvMessageQueue](class.sysvmessagequeue.md), який може бути використаний для доступу до черги повідомлень System V або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція тепер повертає екземпляр [SysvMessageQueue](class.sysvmessagequeue.md); раніше повертався ресурс (resource). |

### Дивіться також

-   [msg\_remove\_queue()](function.msg-remove-queue.md) \- Видалення черги повідомлень
-   [msg\_receive()](function.msg-receive.md) \- Отримання повідомлення з черги повідомлень
-   [msg\_send()](function.msg-send.md) \- Надсилання повідомлення в чергу повідомлень
-   [msg\_stat\_queue()](function.msg-stat-queue.md) \- Отримання інформації із структури даних черги повідомлень
-   [msg\_set\_queue()](function.msg-set-queue.md) \- Встановлення інформації у структурі даних черги повідомлень
