Повертає кількість очікуваних подій у черзі

-   [« inotify\_init](function.inotify-init.html)
    
-   [inotify\_read »](function.inotify-read.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Inotify](ref.inotify.html)
    
-   Повертає кількість очікуваних подій у черзі
    

# inotifyqueuelen

(PECL inotify >= 0.1.2)

inotifyqueuelen — Повертає кількість очікуваних подій у черзі

### Опис

```methodsynopsis
inotify_queue_len(resource $inotify_instance): int
```

Функція дозволяє зрозуміти, чи заблокує [inotify\_read()](function.inotify-read.html) виконання чи ні. Якщо повернене число більше нуля, то в черзі є повідомлення та [inotify\_read()](function.inotify-read.html) не заблокує виконання скрипту.

### Список параметрів

`inotify_instance`

Ресурс, що повертається [inotify\_init()](function.inotify-init.html)

### Значення, що повертаються

Повертає кількість очікуваних повідомлень у черзі.

### Дивіться також

-   [inotify\_init()](function.inotify-init.html) - Ініціалізує екземпляр inotify
-   [stream\_select()](function.stream-select.html) - Запускає еквівалент системного виклику select() на заданих масивах потоків з часом очікування, вказаним параметрами seconds та microseconds
-   [stream\_set\_blocking()](function.stream-set-blocking.html) - Встановити блокуючий/неблокуючий режим у потоці