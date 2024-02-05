---
navigation:
  - streamwrapper.stream-tell.md: '« streamWrapper::stream\_tell'
  - streamwrapper.stream-write.md: 'streamWrapper::stream\_write »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::stream\_truncate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# streamWrapper::stream\_truncate

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

streamWrapper::stream\_truncate - Усічення потоку

### Опис

```methodsynopsis
public streamWrapper::stream_truncate(int $new_size): bool
```

Спрацьовуватиме при усіченні потоку функцією [ftruncate()](function.ftruncate.md)

### Список параметрів

`new_size`

Новий розмір.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ftruncate()](function.ftruncate.md) \- Урізує файл до вказаної довжини
