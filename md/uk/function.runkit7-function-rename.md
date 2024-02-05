---
navigation:
  - function.runkit7-function-remove.md: « runkit7\_function\_remove
  - function.runkit7-import.md: runkit7\_import »
  - index.md: PHP Manual
  - ref.runkit7.md: Функції runkit7
title: runkit7\_function\_rename
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# runkit7\_function\_rename

(PECL runkit7 >= Unknown)

runkit7\_function\_rename — Змінює ім'я функції

### Опис

```methodsynopsis
runkit7_function_rename(string $source_name, string $target_name): bool
```

> **Зауваження**: За замовчуванням, лише функції користувача можуть бути видалені, перейменовані або змінені. Для перекриття внутрішніх функцій, необхідно включити до php.ini опцію `runkit.internal_override`

### Список параметрів

`source_name`

Поточне ім'я функції.

`target_name`

Нове ім'я функції.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [runkit7\_function\_add()](function.runkit7-function-add.md) \- Додає нову функцію, функція аналогічна create\_function
-   [runkit7\_function\_copy()](function.runkit7-function-copy.md) \- Копіює функцію в нове ім'я функції
-   [runkit7\_function\_redefine()](function.runkit7-function-redefine.md) \- замінює визначення функції новою реалізацією
-   [runkit7\_function\_remove()](function.runkit7-function-remove.md) \- Видаляє визначення функції
