---
navigation:
  - ref.filter.md: « Функції фільтрації даних
  - function.filter-id.md: filter\_id »
  - index.md: PHP Manual
  - ref.filter.md: Функції фільтрації даних
title: filter\_has\_var
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# filter\_has\_var

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

filter\_has\_var — Перевіряє існування змінної вказаного типу

### Опис

```methodsynopsis
filter_has_var(int $input_type, string $var_name): bool
```

### Список параметрів

`input_type`

Один из\*\*`INPUT_GET`\*\* **`INPUT_POST`** **`INPUT_COOKIE`** **`INPUT_SERVER`** **`INPUT_ENV`**

`var_name`

Ім'я змінної, що перевіряється.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
