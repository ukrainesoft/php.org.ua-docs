---
navigation:
  - function.sodium-pad.html: « sodiumpad
  - class.sodiumexception.md: SodiumException »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumunpad
---
# sodiumunpad

(PHP 7> = 7.2.0, PHP 8)

sodiumunpad — Видалення даних відступів

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
