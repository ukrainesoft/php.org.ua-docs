Перевірка існування черги повідомлень

-   [« msg\_get\_queue](function.msg-get-queue.html)
    
-   [msg\_receive »](function.msg-receive.html)
    
-   [PHP Manual](index.html)
    
-   [Функции семафоров](ref.sem.html)
    
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

-   [msg\_remove\_queue()](function.msg-remove-queue.html) - Видалення черги повідомлень
-   [msg\_receive()](function.msg-receive.html) - Отримання повідомлення з черги повідомлень
-   [msg\_stat\_queue()](function.msg-stat-queue.html) - Отримання інформації із структури даних черги повідомлень