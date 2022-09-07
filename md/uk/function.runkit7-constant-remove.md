---
navigation:
  - function.runkit7-constant-redefine.md: « runkit7constantredefine
  - function.runkit7-function-add.md: runkit7functionadd »
  - index.md: PHP Manual
  - ref.runkit7.md: Функції runkit7
title: runkit7constantremove
---
# runkit7constantremove

(PECL runkit7> = Unknown)

runkit7constantremove — Видаляє вже певну константу

### Опис

```methodsynopsis
runkit7_constant_remove(string $constant_name): bool
```

### Список параметрів

`constant_name`

Константа, яку потрібно видалити. Або ім'я світової константи, або `classname::constname` видалення константи класу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [define()](function.define.md) - визначає іменовану константу
-   [runkit7constantadd()](function.runkit7-constant-add.md) - Аналогічний define(), але також дозволяє визначити константу класу
-   [runkit7constantredefine()](function.runkit7-constant-redefine.md) - Перевизначає вже певну константу
