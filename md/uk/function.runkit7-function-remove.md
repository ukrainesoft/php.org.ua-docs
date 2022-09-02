---
navigation:
  - function.runkit7-function-redefine.md: « runkit7functionredefine
  - function.runkit7-function-rename.md: runkit7functionrename »
  - index.md: PHP Manual
  - ref.runkit7.md: Функції runkit7
title: runkit7functionremove
---
# runkit7functionremove

(PECL runkit7> = Unknown)

runkit7functionremove — Видалення визначення функції

### Опис

```methodsynopsis
runkit7_function_remove(string $function_name): bool
```

> **Зауваження**: За замовчуванням, лише функції користувача можуть бути видалені, перейменовані або змінені. Для перекриття внутрішніх функцій, необхідно включити до php.ini опцію `runkit.internal_override`

### Список параметрів

`function_name`

Ім'я функції, що видаляється.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [runkit7functionadd()](function.runkit7-function-add.md) - Додає нову функцію, функція аналогічна createfunction
-   [runkit7functioncopy()](function.runkit7-function-copy.md) - Копіює функцію в нове ім'я функції
-   [runkit7functionredefine()](function.runkit7-function-redefine.md) - замінює визначення функції новою реалізацією
-   [runkit7functionrename()](function.runkit7-function-rename.md) - Змінює ім'я функції
