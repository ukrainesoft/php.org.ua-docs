Змінює ім'я функції

-   [« runkit7\_function\_remove](function.runkit7-function-remove.html)
    
-   [runkit7\_import »](function.runkit7-import.html)
    
-   [PHP Manual](index.html)
    
-   [Функции runkit7](ref.runkit7.html)
    
-   Змінює ім'я функції
    

# runkit7functionrename

(PECL runkit7> = Unknown)

runkit7functionrename — Змінює ім'я функції

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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [runkit7\_function\_add()](function.runkit7-function-add.html) - Додає нову функцію, функція аналогічна createfunction
-   [runkit7\_function\_copy()](function.runkit7-function-copy.html) - Копіює функцію в нове ім'я функції
-   [runkit7\_function\_redefine()](function.runkit7-function-redefine.html) - замінює визначення функції новою реалізацією
-   [runkit7\_function\_remove()](function.runkit7-function-remove.html) - Видаляє визначення функції