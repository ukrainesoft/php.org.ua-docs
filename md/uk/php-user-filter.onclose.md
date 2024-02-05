---
navigation:
  - php-user-filter.filter.md: '« php\_user\_filter::filter'
  - php-user-filter.oncreate.md: 'php\_user\_filter::onCreate »'
  - index.md: PHP Manual
  - class.php-user-filter.md: php\_user\_filter
title: 'php\_user\_filter::onClose'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# php\_user\_filter::onClose

(PHP 5, PHP 7, PHP 8)

php\_user\_filter::onClose — Викликається при закритті фільтра

### Опис

```methodsynopsis
public php_user_filter::onClose(): void
```

Цей метод викликається, коли фільтр завершує роботу (зазвичай разом із закриттям потоку), та виконується *після* виклику методу `flush`. Якщо будь-які ресурси були виділені під час виконання методу `onCreate()`, то це час, коли їх час знищувати.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Значення, що повертається, ігнорується.
