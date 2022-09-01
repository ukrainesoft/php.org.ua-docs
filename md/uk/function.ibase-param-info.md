---
navigation:
  - function.ibase-num-params.html: « ibasenumparams
  - function.ibase-pconnect.html: ibasepconnect »
  - index.html: PHP Manual
  - ref.ibase.html: Функции Firebird/InterBase
title: ibaseparaminfo
---
# ibaseparaminfo

(PHP 5, PHP 7 < 7.4.0)

ibaseparaminfo — Повертає інформацію про параметр у підготовленому запиті

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

Повертає масив із такими ключами: `name` `alias` `relation` `length` і `type`

### Дивіться також

-   [ibasefieldinfo()](function.ibase-field-info.html) - Отримує інформацію про поле
-   [ibasenumparams()](function.ibase-num-params.html) - Повертає кількість параметрів у підготовленому запиті
