---
navigation:
  - streamwrapper.rmdir.md: '« streamWrapper::rmdir'
  - streamwrapper.stream-close.md: 'streamWrapper::stream\_close »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::stream\_cast'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# streamWrapper::stream\_cast

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

streamWrapper::stream\_cast — Отримує ресурс рівнем нижче

### Опис

```methodsynopsis
public streamWrapper::stream_cast(int $cast_as): resource
```

Цей метод викликається у процесі виконання [stream\_select()](function.stream-select.md)

### Список параметрів

`cast_as`

Може бути **`STREAM_CAST_FOR_SELECT`**, когда[stream\_select()](function.stream-select.md) викликає **stream\_cast()**, либо\*\*`STREAM_CAST_AS_STREAM`**, когда**stream\_cast()\*\* викликається задля інших цілей.

### Значення, що повертаються

Повинен повернути ресурс потоку, що лежить рівнем нижче, або **`false`**

### Дивіться також

-   [stream\_select()](function.stream-select.md) \- Запускає еквівалент системного виклику select() на заданих масивах потоків з часом очікування, вказаним параметрами seconds та microseconds
