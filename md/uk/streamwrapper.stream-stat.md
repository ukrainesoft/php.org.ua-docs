---
navigation:
  - streamwrapper.stream-set-option.html: '« streamWrapper::streamsetoption'
  - streamwrapper.stream-tell.html: 'streamWrapper::streamtell »'
  - index.html: PHP Manual
  - class.streamwrapper.html: streamWrapper
title: 'streamWrapper::streamстати'
---
# streamWrapper::streamстати

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::streamstat — Отримання інформації про файловий ресурс

### Опис

```methodsynopsis
public streamWrapper::stream_stat(): array|false
```

Цей метод викликається внаслідок виклику функції [fstat()](function.fstat.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Дивіться [stat()](function.stat.html)

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо виклик до цього методу не вдалося (наприклад, не реалізовано).

### Дивіться також

-   [stat()](function.stat.html) - Повертає інформацію про файл
-   [streamwrapper::urlstat()](streamwrapper.url-stat.html) - Отримання інформації про файл
