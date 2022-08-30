Копіює функцію у нове ім'я функції

-   [« runkit7functionadd](function.runkit7-function-add.html)
    
-   [runkit7functionredefine »](function.runkit7-function-redefine.html)
    
-   [PHP Manual](index.md)
    
-   [Функції runkit7](ref.runkit7.md)
    
-   Копіює функцію у нове ім'я функції
    

# runkit7functioncopy

(PECL runkit7> = Unknown)

runkit7functioncopy — Копіює функцію до нового імені функції

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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **runkit7functioncopy()****

```php
<?php
function original() {
  echo "В функции\n";
}
runkit7_function_copy('original','duplicate');
original();
duplicate();
?>
```

Результат виконання цього прикладу:

```
В функции
В функции
```

### Дивіться також

-   [runkit7functionadd()](function.runkit7-function-add.html) - Додає нову функцію, функція аналогічна createfunction
-   [runkit7functionredefine()](function.runkit7-function-redefine.html) - замінює визначення функції новою реалізацією
-   [runkit7functionrename()](function.runkit7-function-rename.html) - Змінює ім'я функції
-   [runkit7functionremove()](function.runkit7-function-remove.html) - Видаляє визначення функції