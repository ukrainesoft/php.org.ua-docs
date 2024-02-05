---
navigation:
  - streamwrapper.destruct.md: '« streamWrapper::\_\_destruct'
  - streamwrapper.dir-opendir.md: 'streamWrapper::dir\_opendir »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::dir\_closedir'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# streamWrapper::dir\_closedir

(PHP 4 >= 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::dir\_closedir — Закрити дескриптор директорії

### Опис

```methodsynopsis
public streamWrapper::dir_closedir(): bool
```

Цей метод викликається у процесі виконання [closedir()](function.closedir.md)

Усі ресурси, заблоковані або виділені під час відкриття та використання потоку директорії, необхідно звільнити.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [closedir()](function.closedir.md) \- Закриває дескриптор каталогу
-   [streamWrapper::dir\_opendir()](streamwrapper.dir-opendir.md) \- відкрити дескриптор директорії
