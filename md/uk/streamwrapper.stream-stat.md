---
navigation:
  - streamwrapper.stream-set-option.md: '« streamWrapper::stream\_set\_option'
  - streamwrapper.stream-tell.md: 'streamWrapper::stream\_tell »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::stream\_stat'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# streamWrapper::stream\_stat

(PHP 4 >= 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::stream\_stat — Отримання інформації про файловий ресурс

### Опис

```methodsynopsis
public streamWrapper::stream_stat(): array|false
```

Цей метод викликається внаслідок виклику функції [fstat()](function.fstat.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Смотрите[stat()](function.stat.md)

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо виклик до цього методу не вдалося (наприклад, не реалізовано).

### Дивіться також

-   [stat()](function.stat.md) \- Повертає інформацію про файл
-   [streamwrapper::url\_stat()](streamwrapper.url-stat.md) \- Отримання інформації про файл
