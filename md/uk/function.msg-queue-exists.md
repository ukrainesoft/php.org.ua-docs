Перевірка існування черги повідомлень

-   [« msggetqueue](function.msg-get-queue.html)
    
-   [msgreceive »](function.msg-receive.html)
    
-   [PHP Manual](index.html)
    
-   [Функції семафорів](ref.sem.html)
    
-   Перевірка існування черги повідомлень
    

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

-   [msgremovequeue()](function.msg-remove-queue.html) - Видалення черги повідомлень
-   [msgreceive()](function.msg-receive.html) - Отримання повідомлення з черги повідомлень
-   [msgstatqueue()](function.msg-stat-queue.html) - Отримання інформації із структури даних черги повідомлень