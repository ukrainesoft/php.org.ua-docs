---
navigation:
  - function.xdiff-string-bdiff.md: « xdiff\_string\_bdiff
  - function.xdiff-string-diff-binary.md: xdiff\_string\_diff\_binary »
  - index.md: PHP Manual
  - ref.xdiff.md: Функції xdiff
title: xdiff\_string\_bpatch
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xdiff\_string\_bpatch

(PECL xdiff >= 1.5.0)

xdiff\_string\_bpatch — Застосування бінарного патча до рядка

### Опис

```methodsynopsis
xdiff_string_bpatch(string $str, string $patch): string
```

Застосовує до рядка `str` бінарний патч `patch`. Ця функція приймає патчі створені як [xdiff\_string\_bdiff()](function.xdiff-string-bdiff.md), так и[xdiff\_string\_rabdiff()](function.xdiff-string-rabdiff.md)

### Список параметрів

`str`

Оригінальний бінарний рядок.

`patch`

Рядок з бінарним патчем.

### Значення, що повертаються

Повертає змінений рядок, або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [xdiff\_string\_bdiff()](function.xdiff-string-bdiff.md) \- Створити бінарний патч для двох рядків
-   [xdiff\_string\_rabdiff()](function.xdiff-string-rabdiff.md) \- Порівняти два рядки та створити бінарний патч використовуючи поліномінальний алгоритм Rabin fingerprint
