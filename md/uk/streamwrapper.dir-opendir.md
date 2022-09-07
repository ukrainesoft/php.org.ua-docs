---
navigation:
  - streamwrapper.dir-closedir.md: '« streamWrapper::dirclosedir'
  - streamwrapper.dir-readdir.md: 'streamWrapper::dirreaddir »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::diropendir'
---
# streamWrapper::diropendir

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::diropendir — Відкрити дескриптор директорії

### Опис

```methodsynopsis
public streamWrapper::dir_opendir(string $path, int $options): bool
```

Цей метод викликається у процесі виконання [opendir()](function.opendir.md)

### Список параметрів

`path`

Задає URL-адресу, яка була передана в [opendir()](function.opendir.md)

> **Зауваження**
> 
> URL можна розділити на частини за допомогою [parseurl()](function.parse-url.md)

`options`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [opendir()](function.opendir.md) - Відкриває дескриптор каталогу
-   [streamWrapper::dirclosedir()](streamwrapper.dir-closedir.md) - Закрити дескриптор директорії
-   [parseurl()](function.parse-url.md) - Розбирає URL та повертає його компоненти
