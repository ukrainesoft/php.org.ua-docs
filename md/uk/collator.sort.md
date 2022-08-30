Сортує масив із використанням зазначеного засобу сортування

-   [« Collator::sortWithSortKeys](collator.sortwithsortkeys.html)
    
-   [NumberFormatter »](class.numberformatter.html)
    
-   [PHP Manual](index.html)
    
-   [Collator](class.collator.html)
    
-   Сортує масив із використанням зазначеного засобу сортування
    

# Collator::sort

# collatorsort

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Collator::sort -- collatorsort — Сортує масив із використанням зазначеного засобу сортування

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public Collator::sort(array &$array, int $flags = Collator::SORT_REGULAR): bool
```

Процедурний стиль

```methodsynopsis
collator_sort(Collator $object, array &$array, int $flags = Collator::SORT_REGULAR): bool
```

Функція сортує масив відповідно до поточних правил локалі.

Еквівалентна стандартній функції PHP [sort()](function.sort.html)

### Список параметрів

`object`

Об'єкт [Collator](class.collator.html)

`array`

Array of strings to sort.

`flags`

Необов'язковий тип сортування, один із таких:

-   **`Collator::SORT_REGULAR`** - порівнює елементи як завжди (не змінюючи тип)
    
-   **`Collator::SORT_NUMERIC`** - порівнює елементи, як числа
    
-   **`Collator::SORT_STRING`** - Порівнює елементи, як рядки
    

Тип сортування за промовчанням - **`Collator::SORT_REGULAR`**. Він також використовується, якщо вказано неприпустиме значення `flags`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **collatorsort()****

```php
<?php
$coll = collator_create( 'en_US' );
$arr  = array( 'at', 'às', 'as' );

var_export( $arr );
collator_sort( $coll, $arr );
var_export( $arr );
?>
```

Результат виконання цього прикладу:

```
array (
  0 => 'at',
  1 => 'às',
  2 => 'as',
)array (
  0 => 'as',
  1 => 'às',
  2 => 'at',
)
```

### Дивіться також

-   [Константы](class.collator.html#intl.collator-constants) [Collator](class.collator.html)
-   [collatorasort()](collator.asort.html) - Сортує масив із збереженням асоціації індексу
-   [collatorsortwithsortkeys()](collator.sortwithsortkeys.html) - Сортує масив з використанням зазначеного Collator та ключів сортування