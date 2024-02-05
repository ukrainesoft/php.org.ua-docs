---
navigation:
  - function.runkit7-constant-redefine.md: « runkit7\_constant\_redefine
  - function.runkit7-function-add.md: runkit7\_function\_add »
  - index.md: PHP Manual
  - ref.runkit7.md: Функції runkit7
title: runkit7\_constant\_remove
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# runkit7\_constant\_remove

(PECL runkit7 >= Unknown)

runkit7\_constant\_remove — Видаляє вже певну константу

### Опис

```methodsynopsis
runkit7_constant_remove(string $constant_name): bool
```

### Список параметрів

`constant_name`

Константа, яку потрібно видалити. Або ім'я світової константи, або `classname::constname` видалення константи класу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [define()](function.define.md) \- визначає іменовану константу
-   [runkit7\_constant\_add()](function.runkit7-constant-add.md) \- Аналогічний define(), але також дозволяє визначити константу класу
-   [runkit7\_constant\_redefine()](function.runkit7-constant-redefine.md) \- Перевизначає вже певну константу
