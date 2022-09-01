---
navigation:
  - ref.runkit7.md: « Функції runkit7
  - function.runkit7-constant-redefine.html: runkit7constantredefine »
  - index.md: PHP Manual
  - ref.runkit7.md: Функції runkit7
title: runkit7constantadd
---
# runkit7constantadd

(PECL runkit7> = Unknown)

runkit7constantadd — Аналогічний define(), але також дозволяє визначити константу класу

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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [define()](function.define.md) - визначає іменовану константу
-   [runkit7constantredefine()](function.runkit7-constant-redefine.html) - Перевизначає вже певну константу
-   [runkit7constantremove()](function.runkit7-constant-remove.html) - Видаляє вже певну константу
