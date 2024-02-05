---
navigation:
  - function.runkit7-function-add.md: « runkit7\_function\_add
  - function.runkit7-function-redefine.md: runkit7\_function\_redefine »
  - index.md: PHP Manual
  - ref.runkit7.md: Функції runkit7
title: runkit7\_function\_copy
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# runkit7\_function\_copy

(PECL runkit7 >= Unknown)

runkit7\_function\_copy — Копіює функцію до нового імені функції

### Опис

```methodsynopsis
runkit7_function_copy(string $source_name, string $target_name): bool
```

### Список параметрів

`source_name`

Ім'я існуючої функції.

`target_name`

Ім'я нової функції, у якому потрібно скопіювати визначення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** runkit7\_function\_copy()\*\*\*\*

```php
<?php
function original() {
  echo "В функции\n";
}
runkit7_function_copy('original','duplicate');
original();
duplicate();
?>
```

Результат виконання наведеного прикладу:

```
В функции
В функции
```

### Дивіться також

-   [runkit7\_function\_add()](function.runkit7-function-add.md) \- Додає нову функцію, функція аналогічна create\_function
-   [runkit7\_function\_redefine()](function.runkit7-function-redefine.md) \- замінює визначення функції новою реалізацією
-   [runkit7\_function\_rename()](function.runkit7-function-rename.md) \- Змінює ім'я функції
-   [runkit7\_function\_remove()](function.runkit7-function-remove.md) \- Видаляє визначення функції
