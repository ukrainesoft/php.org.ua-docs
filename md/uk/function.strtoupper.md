Перетворює рядок у верхній регістр

-   [« strtolower](function.strtolower.html)
    
-   [strtr »](function.strtr.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з рядками](ref.strings.html)
    
-   Перетворює рядок у верхній регістр
    

# strtoupper

(PHP 4, PHP 5, PHP 7, PHP 8)

strtoupper — Перетворює рядок на верхній регістр

### Опис

```methodsynopsis
strtoupper(string $string): string
```

Повертає рядок `string`, де всі літерні символи переведені у верхній регістр.

Приналежність тієї чи іншої символу до буквеним визначається з урахуванням поточної локалі. Це означає, що, наприклад, у локалі "C", що використовується за умовчанням, символ ä не буде перетворений.

### Список параметрів

`string`

Вхідний рядок.

### Значення, що повертаються

Повертає рядок у верхньому регістрі.

### Приклади

**Приклад #1 Приклад використання **strtoupper()****

```php
<?php
$str = "Mary Had A Little Lamb and She LOVED It So";
$str = strtoupper($str);
echo $str; // выводит: MARY HAD A LITTLE LAMB AND SHE LOVED IT SO
?>
```

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [strtolower()](function.strtolower.html) - Перетворює рядок на нижній регістр
-   [ucfirst()](function.ucfirst.html) - Перетворює перший символ рядка у верхній регістр
-   [ucwords()](function.ucwords.html) - Перетворює на верхній регістр перший символ кожного слова в рядку
-   [мбstrtoupper()](function.mb-strtoupper.html) - Приведення рядка до верхнього регістру