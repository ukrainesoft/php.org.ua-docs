---
navigation:
  - streamwrapper.dir-closedir.md: '« streamWrapper::dir\_closedir'
  - streamwrapper.dir-readdir.md: 'streamWrapper::dir\_readdir »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::dir\_opendir'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# streamWrapper::dir\_opendir

(PHP 4 >= 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::dir\_opendir — Відкрити дескриптор директорії

### Опис

```methodsynopsis
public streamWrapper::dir_opendir(string $path, int $options): bool
```

Цей метод викликається у процесі виконання [opendir()](function.opendir.md)

### Список параметрів

`path`

Задає URL-адресу, яка була передана в [opendir()](function.opendir.md)

> **Зауваження** :
> 
> URL можна розділити на частини за допомогою [parse\_url()](function.parse-url.md)

`options`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [opendir()](function.opendir.md) \- Відкриває дескриптор каталогу
-   [streamWrapper::dir\_closedir()](streamwrapper.dir-closedir.md) \- Закрити дескриптор директорії
-   [parse\_url()](function.parse-url.md) \- Розбирає URL та повертає його компоненти
