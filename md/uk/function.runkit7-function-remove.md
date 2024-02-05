---
navigation:
  - function.runkit7-function-redefine.md: « runkit7\_function\_redefine
  - function.runkit7-function-rename.md: runkit7\_function\_rename »
  - index.md: PHP Manual
  - ref.runkit7.md: Функції runkit7
title: runkit7\_function\_remove
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# runkit7\_function\_remove

(PECL runkit7 >= Unknown)

runkit7\_function\_remove — Видалення визначення функції

### Опис

```methodsynopsis
runkit7_function_remove(string $function_name): bool
```

> **Зауваження**: За замовчуванням, лише функції користувача можуть бути видалені, перейменовані або змінені. Для перекриття внутрішніх функцій, необхідно включити до php.ini опцію `runkit.internal_override`

### Список параметрів

`function_name`

Ім'я функції, що видаляється.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [runkit7\_function\_add()](function.runkit7-function-add.md) \- Додає нову функцію, функція аналогічна create\_function
-   [runkit7\_function\_copy()](function.runkit7-function-copy.md) \- Копіює функцію в нове ім'я функції
-   [runkit7\_function\_redefine()](function.runkit7-function-redefine.md) \- замінює визначення функції новою реалізацією
-   [runkit7\_function\_rename()](function.runkit7-function-rename.md) \- Змінює ім'я функції
