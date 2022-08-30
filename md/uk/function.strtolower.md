Перетворює рядок на нижній регістр

-   [« strtok](function.strtok.html)
    
-   [strtoupper »](function.strtoupper.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з рядками](ref.strings.html)
    
-   Перетворює рядок на нижній регістр
    

# strtolower

(PHP 4, PHP 5, PHP 7, PHP 8)

strtolower — Перетворює рядок на нижній регістр

### Опис

```methodsynopsis
strtolower(string $string): string
```

Повертає рядок `string`, де всі літерні символи переведені в нижній регістр.

Приналежність тієї чи іншої символу до буквеним визначається з урахуванням поточної локалі. Це означає, що, наприклад, у локалі "C", що використовується за умовчанням, символ Ä не буде перетворений.

### Список параметрів

`string`

Вхідний рядок.

### Значення, що повертаються

Повертає рядок у нижньому регістрі.

### Приклади

**Приклад #1 Приклад використання **strtolower()****

```php
<?php
$str = "Mary Had A Little Lamb and She LOVED It So";
$str = strtolower($str);
echo $str; // выводит: mary had a little lamb and she loved it so
?>
```

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [strtoupper()](function.strtoupper.html) - Перетворює рядок у верхній регістр
-   [ucfirst()](function.ucfirst.html) - Перетворює перший символ рядка у верхній регістр
-   [ucwords()](function.ucwords.html) - Перетворює на верхній регістр перший символ кожного слова в рядку
-   [мбstrtolower()](function.mb-strtolower.html) - Приведення рядка до нижнього регістру