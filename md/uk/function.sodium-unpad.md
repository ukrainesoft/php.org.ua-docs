---
navigation:
  - function.sodium-pad.md: « sodium\_pad
  - class.sodiumexception.md: SodiumException »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_unpad
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_unpad

(PHP 7 >= 7.2.0, PHP 8)

sodium\_unpad — Видалення даних відступів

### Опис

```methodsynopsis
sodium_unpad(string $string, int $block_size): string
```

Видаляє дані відступів у доповненого рядка. Безпечна за часом.

### Список параметрів

`string`

Доповнений рядок.

`block_size`

Розмір блоку заповнення.

### Значення, що повертаються

Стоку з віддаленими відступами.
