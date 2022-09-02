---
navigation:
  - function.inflate-get-read-len.md: « inflategetreadlen
  - function.inflate-init.md: inflateinit »
  - index.md: PHP Manual
  - ref.zlib.md: Функции Zlib
title: inflategetstatus
---
# inflategetstatus

(PHP 7> = 7.2.0, PHP 8)

inflategetstatus — Отримує статус декомпресії

### Опис

```methodsynopsis
inflate_get_status(InflateContext $context): int
```

Зазвичай повертає **`ZLIB_OK`** або **`ZLIB_STREAM_END`**

### Список параметрів

`context`

### Значення, що повертаються

Повертає статус декомпресії або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `context` чекає на екземпляр [InflateContext](class.inflatecontext.md); раніше, очікувався ресурс (resource). |
