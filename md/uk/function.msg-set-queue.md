---
navigation:
  - function.msg-send.md: « msgsend
  - function.msg-stat-queue.md: msgstatqueue »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: msgsetqueue
---
# msgsetqueue

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

msgsetqueue — Встановлення інформації у структурі даних черги повідомлень

### Опис

```methodsynopsis
msg_set_queue(SysvMessageQueue $queue, array $data): bool
```

**msgsetqueue()** дозволяє змінити значення полів msgperm.uid, msgperm.gid, msgperm.mode та msgqbytes у службовій структурі даних черги повідомлень.

Зміна структури даних можлива лише в тому випадку, якщо PHP запущений від користувача, який створив чергу, що володіє чергою (визначається полем msgperm.xxx), або має root-привілеї. Root-привілеї потрібні для збільшення значення msgqbytes вище системних лімітів.

### Список параметрів

`queue`

Черга повідомлень.

`data`

Ви вказуєте значення, що вимагають встановлення через відповідні ключі масиву `data`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `queue` тепер чекає екземпляр [SysvMessageQueue](class.sysvmessagequeue.md); раніше очікувався ресурс (resource). |

### Дивіться також

-   [msgremovequeue()](function.msg-remove-queue.md) - Видалення черги повідомлень
-   [msgreceive()](function.msg-receive.md) - Отримання повідомлення з черги повідомлень
-   [msgstatqueue()](function.msg-stat-queue.md) - Отримання інформації із структури даних черги повідомлень
-   [msggetqueue()](function.msg-get-queue.md) - Створення або підключення до черги повідомлень
