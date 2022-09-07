---
navigation:
  - streamwrapper.stream-tell.md: '« streamWrapper::streamtell'
  - streamwrapper.stream-write.md: 'streamWrapper::streamwrite »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::streamtruncate'
---
# streamWrapper::streamtruncate

(PHP 5> = 5.4.0, PHP 7, PHP 8)

streamWrapper::streamtruncate - Усічення потоку

### Опис

```methodsynopsis
public streamWrapper::stream_truncate(int $new_size): bool
```

Спрацьовуватиме при усіченні потоку функцією [ftruncate()](function.ftruncate.md)

### Список параметрів

`new_size`

Новий розмір.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ftruncate()](function.ftruncate.md) - Урізує файл до вказаної довжини
