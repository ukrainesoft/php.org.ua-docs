Викликається під час закриття фільтра

-   [« php\_user\_filter::filter](php-user-filter.filter.html)
    
-   [php\_user\_filter::onCreate »](php-user-filter.oncreate.html)
    
-   [PHP Manual](index.html)
    
-   [php\_user\_filter](class.php-user-filter.html)
    
-   Викликається під час закриття фільтра
    

# phpuserfilter::onClose

(PHP 5, PHP 7, PHP 8)

phpuserfilter::onClose — Викликається при закритті фільтра

### Опис

```methodsynopsis
public php_user_filter::onClose(): void
```

Цей метод викликається, коли фільтр завершує роботу (зазвичай разом із закриттям потоку), та виконується *після* виклику методу `flush`. Якщо будь-які ресурси були виділені під час виконання методу `onCreate()`, то це час, коли їх час знищувати.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Значення, що повертається, ігнорується.