---
navigation:
  - streamwrapper.stream-close.md: '« streamWrapper::stream\_close'
  - streamwrapper.stream-flush.md: 'streamWrapper::stream\_flush »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::stream\_eof'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# streamWrapper::stream\_eof

(PHP 4 >= 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::stream\_eof — Перевіряє досягнення кінця файлу за вказівником файлу

### Опис

```methodsynopsis
public streamWrapper::stream_eof(): bool
```

Цей метод викликається в результаті виклику [feof()](function.feof.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повинен повернути \*\*`true`\*\*якщо позиція читання/запису знаходиться в кінці потоку і доступних для читання даних більше немає. В інших випадках повертається **`false`**

### Примітки

**Увага**

При читанні файлу повністю (наприклад, функцією [file\_get\_contents()](function.file-get-contents.md)), PHP буде викликати [streamWrapper::stream\_read()](streamwrapper.stream-read.md)и вместе с ним\*\*streamWrapper::stream\_eof()\*\*в цикле, пока[streamWrapper::stream\_read()](streamwrapper.stream-read.md) повертає непустий рядок. Повертається з **streamWrapper::stream\_eof()** значення у своїй ігнорується.

### Дивіться також

-   [feof()](function.feof.md) \- Перевіряє, чи кінець файлу досягнуто
