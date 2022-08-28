Динамічно змінює ім'я заданого методу

-   [« runkit7\_method\_remove](function.runkit7-method-remove.html)
    
-   [runkit7\_object\_id »](function.runkit7-object-id.html)
    
-   [PHP Manual](index.html)
    
-   [Функции runkit7](ref.runkit7.html)
    
-   Динамічно змінює ім'я заданого методу
    

# runkit7методrename

(PECL runkit7> = Unknown)

runkit7методrename - Динамічно змінює ім'я заданого методу

### Опис

```methodsynopsis
runkit7_method_rename(string $class_name, string $source_method_name, string $target_method_name): bool
```

> **Зауваження**: Ця функція не може бути використана для впливу на працюючі в даний момент (або ланцюгові) методи.

### Список параметрів

`class_name`

Клас, у якому необхідно перейменувати спосіб.

`source_method_name`

Метод, який слід перейменувати.

`target_method_name`

Нове ім'я методу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **runkit7методrename()****

```php
<?php
class Example {
    function foo() {
        return "foo!\n";
    }
}

// Переименование метода 'foo' в 'bar'
runkit7_method_rename(
    'Example',
    'foo',
    'bar'
);

// Вывод переименованной функции
echo (new Example)->bar();
?>
```

Результат виконання цього прикладу:

```
foo!
```

### Дивіться також

-   [runkit7\_method\_add()](function.runkit7-method-add.html) - Динамічно додає новий метод у заданий клас
-   [runkit7\_method\_copy()](function.runkit7-method-copy.html) - Копіює метод з одного класу до іншого
-   [runkit7\_method\_redefine()](function.runkit7-method-redefine.html) - динамічно змінює код заданого методу
-   [runkit7\_method\_remove()](function.runkit7-method-remove.html) - динамічно видаляє заданий метод
-   [runkit7\_function\_rename()](function.runkit7-function-rename.html) - Змінює ім'я функції