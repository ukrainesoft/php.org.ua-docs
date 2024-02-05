---
navigation:
  - function.runkit7-constant-add.md: « runkit7\_constant\_add
  - function.runkit7-constant-remove.md: runkit7\_constant\_remove »
  - index.md: PHP Manual
  - ref.runkit7.md: Функції runkit7
title: runkit7\_constant\_redefine
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# runkit7\_constant\_redefine

(PECL runkit7 >= Unknown)

runkit7\_constant\_redefine - Перевизначає вже певну константу

### Опис

```methodsynopsis
runkit7_constant_redefine(string $constant_name, mixed $value, int $new_visibility = ?): bool
```

### Список параметрів

`constant_name`

Константа, яку потрібно перевизначити. Або ім'я світової константи, або `classname::constname` для перевизначення константи класу.

`value`

Значення, яке присвоюється константі.

`new_visibility`

Нова видимість константи для констант класу. За промовчанням без змін. Одна з констант **`RUNKIT7_ACC_*`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [runkit7\_constant\_add()](function.runkit7-constant-add.md) \- Аналогічний define(), але також дозволяє визначити константу класу
-   [runkit7\_constant\_remove()](function.runkit7-constant-remove.md) \- Видаляє вже певну константу
