---
navigation:
  - ref.runkit7.md: « Функції runkit7
  - function.runkit7-constant-redefine.md: runkit7\_constant\_redefine »
  - index.md: PHP Manual
  - ref.runkit7.md: Функції runkit7
title: runkit7\_constant\_add
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# runkit7\_constant\_add

(PECL runkit7 >= Unknown)

runkit7\_constant\_add — Аналогічний define(), але також дозволяє визначити константу класу

### Опис

```methodsynopsis
runkit7_constant_add(string $constant_name, mixed $value, int $newVisibility = ?): bool
```

### Список параметрів

`constant_name`

Ім'я константи, що оголошується. Або рядок для позначення глобальної константи, або `classname::constname` визначення константи класу.

`value`

Значення константи (NULL, Bool, Long, Double, String, Array чи Resource).

`newVisibility`

Видимість константи для констант класу. За замовчуванням є загальнодоступним. Одна з констант **`RUNKIT7_ACC_*`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [define()](function.define.md) \- визначає іменовану константу
-   [runkit7\_constant\_redefine()](function.runkit7-constant-redefine.md) \- Перевизначає вже певну константу
-   [runkit7\_constant\_remove()](function.runkit7-constant-remove.md) \- Видаляє вже певну константу
