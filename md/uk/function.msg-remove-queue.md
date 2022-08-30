Видалення черги повідомлень

-   [« msgreceive](function.msg-receive.html)
    
-   [msgsend »](function.msg-send.html)
    
-   [PHP Manual](index.md)
    
-   [Функції семафорів](ref.sem.md)
    
-   Видалення черги повідомлень
    

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

-   [msggetqueue()](function.msg-get-queue.html) - Створення або підключення до черги повідомлень
-   [msgreceive()](function.msg-receive.html) - Отримання повідомлення з черги повідомлень
-   [msgstatqueue()](function.msg-stat-queue.html) - Отримання інформації із структури даних черги повідомлень
-   [msgsetqueue()](function.msg-set-queue.html) - Встановлення інформації у структурі даних черги повідомлень