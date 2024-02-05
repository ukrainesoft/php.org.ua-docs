---
navigation:
  - function.inflate-get-read-len.md: « inflate\_get\_read\_len
  - function.inflate-init.md: inflate\_init »
  - index.md: PHP Manual
  - ref.zlib.md: Функції Zlib
title: inflate\_get\_status
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# inflate\_get\_status

(PHP 7 >= 7.2.0, PHP 8)

inflate\_get\_status — Отримує статус декомпресії

### Опис

```methodsynopsis
inflate_get_status(InflateContext $context): int
```

Зазвичай повертає **`ZLIB_OK`** або **`ZLIB_STREAM_END`**

### Список параметрів

`context`

### Значення, що повертаються

Повертає статус декомпресії.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `context` чекає на екземпляр [InflateContext](class.inflatecontext.md); раніше, очікувався ресурс (resource). |
