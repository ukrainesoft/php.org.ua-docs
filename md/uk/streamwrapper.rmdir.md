---
navigation:
  - streamwrapper.rename.md: '« streamWrapper::rename'
  - streamwrapper.stream-cast.md: 'streamWrapper::stream\_cast »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::rmdir'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# streamWrapper::rmdir

(PHP 5, PHP 7, PHP 8)

streamWrapper::rmdir — Видаляє директорію

### Опис

```methodsynopsis
public streamWrapper::rmdir(string $path, int $options): bool
```

Цей метод викликається у процесі виконання [rmdir()](function.rmdir.md)

> **Зауваження** :
> 
> Щоб повідомлення про помилки відповідали реальним помилкам, цей метод *не потрібно* визначати у випадках, коли обгортка не підтримує видалення директорій.

### Список параметрів

`path`

URL директорії, що видаляється.

`options`

Бітова маска, складена з констант, начебто **`STREAM_MKDIR_RECURSIVE`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо виклик до цього методу не вдалося (наприклад, не реалізовано).

### Примітки

> **Зауваження** :
> 
> Властивість streamWrapper::$context буде оновлено, якщо коректний контекст був переданий у функцію, що викликається.

### Дивіться також

-   [rmdir()](function.rmdir.md) \- видаляє директорію
-   [streamwrapper::mkdir()](streamwrapper.mkdir.md) \- створення директорії
-   [streamwrapper::unlink()](streamwrapper.unlink.md) \- Видалення файлу
