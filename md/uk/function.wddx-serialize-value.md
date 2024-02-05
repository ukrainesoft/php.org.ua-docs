---
navigation:
  - function.wddx-packet-start.md: « wddx\_packet\_start
  - function.wddx-serialize-vars.md: wddx\_serialize\_vars »
  - index.md: PHP Manual
  - ref.wddx.md: Функції WDDX
title: wddx\_serialize\_value
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wddx\_serialize\_value

(PHP 4, PHP 5, PHP 7)

wddx\_serialize\_value - Серіалізує одне значення всередині пакету WDDX

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 7.4.0.

### Опис

```methodsynopsis
wddx_serialize_value(mixed $var, string $comment = ?): string
```

Створює пакет WDDX з заданого значення.

### Список параметрів

`var`

Значення для серіалізації

`comment`

Необов'язковий рядок із коментарем, який відображається в заголовку пакета.

### Значення, що повертаються

Повертає пакет WDDX або \*\*`false`\*\*в случае возникновения ошибки.
