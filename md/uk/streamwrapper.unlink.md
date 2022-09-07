---
navigation:
  - streamwrapper.stream-write.md: '« streamWrapper::streamwrite'
  - streamwrapper.url-stat.md: 'streamWrapper::urlstat »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::unlink'
---
# streamWrapper::unlink

(PHP 5, PHP 7, PHP 8)

streamWrapper::unlink — Видалення файлу

### Опис

```methodsynopsis
public streamWrapper::unlink(string $path): bool
```

Цей метод викликається у процесі виконання [unlink()](function.unlink.md)

> **Зауваження**
> 
> Щоб повідомлення про помилки відповідали реальним помилкам, цей метод *не потрібно* визначати у випадках, коли обгортка не підтримує видалення файлів.

### Список параметрів

`path`

URL файлу, що видаляється.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо виклик до цього методу не вдалося (наприклад, не реалізовано).

### Примітки

> **Зауваження**
> 
> Властивість streamWrapper::$context буде оновлено, якщо коректний контекст був переданий у функцію, що викликається.

### Дивіться також

-   [unlink()](function.unlink.md) - Видаляє файл
-   [streamWrapper::rmdir()](streamwrapper.rmdir.md) - видаляє директорію
