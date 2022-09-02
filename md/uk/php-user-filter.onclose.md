---
navigation:
  - php-user-filter.filter.md: '« phpuserfilter::filter'
  - php-user-filter.oncreate.md: 'phpuserfilter::onCreate »'
  - index.md: PHP Manual
  - class.php-user-filter.md: phpuserfilter
title: 'phpuserfilter::onClose'
---
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
