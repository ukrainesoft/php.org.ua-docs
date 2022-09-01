---
navigation:
  - function.ftok.md: « ftok
  - function.msg-queue-exists.html: msgqueueexists »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: msggetqueue
---
# msggetqueue

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

msggetqueue — Створення або підключення до черги повідомлень

### Опис

```methodsynopsis
msg_get_queue(int $key, int $permissions = 0666): SysvMessageQueue|false
```

**msggetqueue()** повертає ідентифікатор, який використовується для доступу до черги повідомлень System V із зазначеним ключем `key`. Перший виклик створює чергу повідомлень із необов'язковими правами `permissions`. Другий та наступні виклики **msggetqueue()** для того ж `key` повертатимуть інші ідентифікатори, проте всі вони посилатимуться на ту саму чергу повідомлень.

### Список параметрів

`key`

Числовий ідентифікатор черги повідомлень.

`permissions`

Права доступу до черги. За промовчанням 0666. Якщо черга повідомлень вже існує, параметр `permissions` ігнорується.

### Значення, що повертаються

Повертає екземпляр [SysvMessageQueue](class.sysvmessagequeue.md), який може бути використаний для доступу до черги повідомлень System V або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція тепер повертає екземпляр [SysvMessageQueue](class.sysvmessagequeue.md); раніше повертався ресурс (resource). |

### Дивіться також

-   [msgremovequeue()](function.msg-remove-queue.html) - Видалення черги повідомлень
-   [msgreceive()](function.msg-receive.html) - Отримання повідомлення з черги повідомлень
-   [msgsend()](function.msg-send.html) - Надсилання повідомлення в чергу повідомлень
-   [msgstatqueue()](function.msg-stat-queue.html) - Отримання інформації із структури даних черги повідомлень
-   [msgsetqueue()](function.msg-set-queue.html) - Встановлення інформації у структурі даних черги повідомлень
