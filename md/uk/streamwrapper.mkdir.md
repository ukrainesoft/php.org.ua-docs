---
navigation:
  - streamwrapper.dir-rewinddir.md: '« streamWrapper::dirrewinddir'
  - streamwrapper.rename.md: 'streamWrapper::rename »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::mkdir'
---
# streamWrapper::mkdir

(PHP 5, PHP 7, PHP 8)

streamWrapper::mkdir — Створення директорії

### Опис

```methodsynopsis
public streamWrapper::mkdir(string $path, int $mode, int $options): bool
```

Цей метод викликається у процесі виконання [mkdir()](function.mkdir.md)

> **Зауваження**
> 
> Щоб повідомлення про помилки відповідали реальним помилкам, цей метод *не потрібно* визначати у випадках, коли обгортка не підтримує створення директорій.

### Список параметрів

`path`

Створювана директорія.

`mode`

Значення, передане в [mkdir()](function.mkdir.md)

`options`

Бітова маска, складена з констант, начебто **`STREAM_MKDIR_RECURSIVE`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо виклик до цього методу не вдалося (наприклад, не реалізовано).

### Примітки

> **Зауваження**
> 
> Властивість streamWrapper::$context буде оновлено, якщо коректний контекст був переданий у функцію, що викликається.

### Дивіться також

-   [mkdir()](function.mkdir.md) - створює директорію
-   [streamwrapper::rmdir()](streamwrapper.rmdir.md) - видаляє директорію
