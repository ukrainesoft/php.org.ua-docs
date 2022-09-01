---
navigation:
  - streamwrapper.destruct.md: '« streamWrapper::destruct'
  - streamwrapper.dir-opendir.html: 'streamWrapper::diropendir »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::dirclosedir'
---
# streamWrapper::dirclosedir

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::dirclosedir — Закрити дескриптор директорії

### Опис

```methodsynopsis
public streamWrapper::dir_closedir(): bool
```

Цей метод викликається у процесі виконання [closedir()](function.closedir.md)

Усі ресурси, заблоковані або виділені під час відкриття та використання потоку директорії, необхідно звільнити.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [closedir()](function.closedir.md) - Закриває дескриптор каталогу
-   [streamWrapper::diropendir()](streamwrapper.dir-opendir.md) - відкрити дескриптор директорії
