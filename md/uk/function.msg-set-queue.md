---
navigation:
  - function.msg-send.md: « msg\_send
  - function.msg-stat-queue.md: msg\_stat\_queue »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: msg\_set\_queue
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# msg\_set\_queue

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

msg\_set\_queue — Встановлення інформації у структурі даних черги повідомлень

### Опис

```methodsynopsis
msg_set_queue(SysvMessageQueue $queue, array $data): bool
```

\*\*msg\_set\_queue()\*\*позволяет вам изменить значения полей msg\_perm.uid, msg\_perm.gid, msg\_perm.mode та msg\_qbytes у службовій структурі даних черги повідомлень.

Зміна структури даних можлива лише в тому випадку, якщо PHP запущений від користувача, який створив чергу, що володіє чергою (визначається полем msg\_perm.xxx), або має root-привілеї. Root-привілеї потрібні для збільшення значення msg\_qbytes вище системних лімітів.

### Список параметрів

`queue`

Черга повідомлень.

`data`

Ви вказуєте значення, що вимагають встановлення через відповідні ключі масиву `data`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`queue` тепер чекає екземпляр [SysvMessageQueue](class.sysvmessagequeue.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [msg\_remove\_queue()](function.msg-remove-queue.md) \- Видалення черги повідомлень
-   [msg\_receive()](function.msg-receive.md) \- Отримання повідомлення з черги повідомлень
-   [msg\_stat\_queue()](function.msg-stat-queue.md) \- Отримання інформації із структури даних черги повідомлень
-   [msg\_get\_queue()](function.msg-get-queue.md) \- Створення або підключення до черги повідомлень
