---
navigation:
  - streamwrapper.stream-set-option.md: '« streamWrapper::streamsetoption'
  - streamwrapper.stream-tell.md: 'streamWrapper::streamtell »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::streamстати'
---
# streamWrapper::streamстати

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::streamstat — Отримання інформації про файловий ресурс

### Опис

```methodsynopsis
public streamWrapper::stream_stat(): array|false
```

Цей метод викликається внаслідок виклику функції [fstat()](function.fstat.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Дивіться [stat()](function.stat.md)

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо виклик до цього методу не вдалося (наприклад, не реалізовано).

### Дивіться також

-   [stat()](function.stat.md) - Повертає інформацію про файл
-   [streamwrapper::urlstat()](streamwrapper.url-stat.md) - Отримання інформації про файл
