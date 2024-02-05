---
navigation:
  - function.variant-set-type.md: « variant\_set\_type
  - function.variant-sub.md: variant\_sub »
  - index.md: PHP Manual
  - ref.com.md: Функції COM
title: variant\_set
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# variant\_set

(PHP 5, PHP 7, PHP 8)

variant\_set — Присвоєння нового значення об'єкту варіанта

### Опис

```methodsynopsis
variant_set(variant $variant, mixed $value): void
```

Перетворює значення параметра `value` у варіант і надає його об'єкту `variant`; при цьому новий об'єкт не створюється і старе значення об'єкта `variant` пропадає.

### Список параметрів

`variant`

Варіант.

`value`

### Значення, що повертаються

Функція не повертає значення після виконання.
