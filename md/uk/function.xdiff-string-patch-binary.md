---
navigation:
  - function.xdiff-string-merge3.md: « xdiff\_string\_merge3
  - function.xdiff-string-patch.md: xdiff\_string\_patch »
  - index.md: PHP Manual
  - ref.xdiff.md: Функції xdiff
title: xdiff\_string\_patch\_binary
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xdiff\_string\_patch\_binary

(PECL xdiff >= 0.2.0)

xdiff\_string\_patch\_binary — Псевдоним[xdiff\_string\_bpatch()](function.xdiff-string-bpatch.md)

### Опис

```methodsynopsis
xdiff_string_patch_binary(string $str, string $patch): string
```

Застосовує до рядка `str` бінарний патч `patch`. Ця функція приймає патчі створені як [xdiff\_string\_bdiff()](function.xdiff-string-bdiff.md), так и[xdiff\_string\_rabdiff()](function.xdiff-string-rabdiff.md)

Починаючи з версії 1.5.0 є псевдонімом для [xdiff\_string\_bpatch()](function.xdiff-string-bpatch.md)

### Список параметрів

`str`

Оригінальний бінарний рядок.

`patch`

Рядок з бінарним патчем.

### Значення, що повертаються

Повертає змінений рядок, або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [xdiff\_string\_bpatch()](function.xdiff-string-bpatch.md) \- Застосування бінарного патча до рядка
-   [xdiff\_string\_bdiff()](function.xdiff-string-bdiff.md) \- Створити бінарний патч для двох рядків
-   [xdiff\_string\_rabdiff()](function.xdiff-string-rabdiff.md) \- Порівняти два рядки та створити бінарний патч використовуючи поліномінальний алгоритм Rabin fingerprint
