---
navigation:
  - function.inflate-add.md: « inflate\_add
  - function.inflate-get-status.md: inflate\_get\_status »
  - index.md: PHP Manual
  - ref.zlib.md: Функції Zlib
title: inflate\_get\_read\_len
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# inflate\_get\_read\_len

(PHP 7 >= 7.2.0, PHP 8)

inflate\_get\_read\_len — Отримує кількість прочитаних байт

### Опис

```methodsynopsis
inflate_get_read_len(InflateContext $context): int
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`context`

### Значення, що повертаються

Повертає кількість прочитаних байт або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `context` чекає на екземпляр [InflateContext](class.inflatecontext.md); раніше, очікувався ресурс (resource). |
