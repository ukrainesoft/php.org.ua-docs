Видаляє визначення функції

-   [« runkit7\_function\_redefine](function.runkit7-function-redefine.html)
    
-   [runkit7\_function\_rename »](function.runkit7-function-rename.html)
    
-   [PHP Manual](index.html)
    
-   [Функции runkit7](ref.runkit7.html)
    
-   Видаляє визначення функції
    

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

-   [runkit7\_function\_add()](function.runkit7-function-add.html) - Додає нову функцію, функція аналогічна createfunction
-   [runkit7\_function\_copy()](function.runkit7-function-copy.html) - Копіює функцію в нове ім'я функції
-   [runkit7\_function\_redefine()](function.runkit7-function-redefine.html) - замінює визначення функції новою реалізацією
-   [runkit7\_function\_rename()](function.runkit7-function-rename.html) - Змінює ім'я функції