---
navigation:
  - function.ibase-num-params.md: « ibase\_num\_params
  - function.ibase-pconnect.md: ibase\_pconnect »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_param\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_param\_info

(PHP 5, PHP 7 < 7.4.0)

ibase\_param\_info — Повертає інформацію про параметр у підготовленому запиті

### Опис

```methodsynopsis
ibase_param_info(resource $query, int $param_number): array
```

Повертає масив з інформацією щодо параметра після підготовки запиту.

### Список параметрів

`query`

Дескриптор підготовленого запиту InterBase

`param_number`

Зміщення параметра.

### Значення, що повертаються

Повертає масив із такими ключами: `name` `alias` `relation` `length`и`type`

### Дивіться також

-   [ibase\_field\_info()](function.ibase-field-info.md) \- Отримує інформацію про поле
-   [ibase\_num\_params()](function.ibase-num-params.md) \- Повертає кількість параметрів у підготовленому запиті
