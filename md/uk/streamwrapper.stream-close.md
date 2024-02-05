---
navigation:
  - streamwrapper.stream-cast.md: '« streamWrapper::stream\_cast'
  - streamwrapper.stream-eof.md: 'streamWrapper::stream\_eof »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::stream\_close'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# streamWrapper::stream\_close

(PHP 4 >= 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::stream\_close — Закриває ресурс

### Опис

```methodsynopsis
public streamWrapper::stream_close(): void
```

Цей метод викликається у процесі виконання [fclose()](function.fclose.md)

Усі ресурси, виділені або заблоковані обгорткою, мають бути звільнені.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [fclose()](function.fclose.md) \- Закриває відкритий дескриптор файлу
-   [streamWrapper::dir\_closedir()](streamwrapper.dir-closedir.md) \- Закрити дескриптор директорії
