Читає повідомлення, що очікують, з черги

-   [« inotifyqueuelen](function.inotify-queue-len.html)
    
-   [inotifyрмwatch »](function.inotify-rm-watch.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Inotify](ref.inotify.html)
    
-   Читає повідомлення, що очікують, з черги
    

# inotifyread

(PECL inotify >= 0.1.2)

inotifyread — Читає повідомлення, що очікують, з черги

### Опис

```methodsynopsis
inotify_read(resource $inotify_instance): array
```

Читає повідомлення з черги.

### Список параметрів

`inotify_instance`

Ресурс, що повертається [inotifyinit()](function.inotify-init.html)

### Значення, що повертаються

Масив подій inotify або **`false`**, якщо подій у черзі немає та `inotify_instance` не блокуючий. Кожен елемент масиву складається з:

-   wd - дескриптор спостерігача, повернутий [inotifyaddwatch()](function.inotify-add-watch.html)
-   mask - бітова маска [событий](inotify.constants.html)
-   cookie – унікальний ідентифікатор для об'єднання пов'язаних подій (наприклад **`IN_MOVE_FROM`** і **`IN_MOVE_TO`**
-   name - ім'я файлу (наприклад якщо в директорії, що спостерігається, змінився файл)

### Дивіться також

-   [inotifyinit()](function.inotify-init.html) - Ініціалізує екземпляр inotify
-   [streamselect()](function.stream-select.html) - Запускає еквівалент системного виклику select() на заданих масивах потоків з часом очікування, вказаним параметрами seconds та microseconds
-   [streamsetblocking()](function.stream-set-blocking.html) - Встановити блокуючий/неблокуючий режим у потоці
-   [inotifyqueuelen()](function.inotify-queue-len.html) - Повертає кількість очікуваних подій у черзі