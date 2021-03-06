- [«msg_send](function.msg-send.md)
- [msg_stat_queue »](function.msg-stat-queue.md)

- [PHP Manual](index.md)
- [Функції семафорів](ref.sem.md)
- Встановлення інформації у структурі даних черги повідомлень

# msg_set_queue

(PHP 4 \>= 4.3.0, PHP 5, PHP 7, PHP 8)

msg_set_queue — Встановлення інформації у структурі даних черги
повідомлень

### Опис

**msg_set_queue**([SysvMessageQueue](class.sysvmessagequeue.md)
`$queue`, array `$data`): bool

**msg_set_queue()** дозволяє змінити значення полів msg_perm.uid,
msg_perm.gid, msg_perm.mode та msg_qbytes у службовій структурі даних
черги повідомлень.

Зміна структури даних можлива лише в тому випадку, якщо PHP
запущений від користувача, який створив чергу, що володіє чергою
(визначається полем msg_perm.xxx) або має root-привілеї.
Root-привілеї потрібні для збільшення значення msg_qbytes вище
системних лімітів.

### Список параметрів

`queue`
Черга повідомлень.

`data`
Ви вказуєте значення, що вимагають, через відповідні ключі
масиву `data`.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Список змін

| Версія | Опис                                                                                                                        |
|--------|-----------------------------------------------------------------------------------------------------------------------------|
| 8.0.0  | Параметр queue тепер очікує на екземпляр [SysvMessageQueue](class.sysvmessagequeue.md); раніше очікували ресурс (resource). |

### Дивіться також

- [msg_remove_queue()](function.msg-remove-queue.md) - Видалення
черги повідомлень
- [msg_receive()](function.msg-receive.md) - Отримання повідомлення з
черги повідомлень
- [msg_stat_queue()](function.msg-stat-queue.md) - Отримання
інформації із структури даних черги повідомлень
- [msg_get_queue()](function.msg-get-queue.md) - Створення або
підключення до черги повідомлень
