Сортує масив з використанням зазначеного Collator та ключів сортування

-   [« Collator::setStrength](collator.setstrength.html)
    
-   [Collator::sort »](collator.sort.html)
    
-   [PHP Manual](index.html)
    
-   [Collator](class.collator.html)
    
-   Сортує масив з використанням зазначеного Collator та ключів сортування
    

# Collator::sortWithSortKeys

# collatorsortwithsortkeys

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Collator::sortWithSortKeys -- collatorsortwithsortkeys — Сортує масив з використанням вказаного Collator та ключів сортування

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public Collator::sortWithSortKeys(array &$array): bool
```

Процедурний стиль

```methodsynopsis
collator_sort_with_sort_keys(Collator $object, array &$array): bool
```

Те саме, що і [collator\_sort()](collator.sort.html), але використовує ключі сортування ICU, створені ucolgetSortKey() збільшення швидкості роботи з великими масивами.

### Список параметрів

`object`

Об'єкт [Collator](class.collator.html)

`array`

Масив рядків для сортування

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **collatorsortwithsortkeys()****

```php
<?php
$arr  = array( 'Köpfe', 'Kypper', 'Kopfe' );
$coll = collator_create( 'sv' );

collator_sort_with_sort_keys( $coll, $arr );
var_export( $arr );
?>
```

Результат виконання цього прикладу:

```
array (
  0 => 'Kopfe',
  1 => 'Kypper',
  2 => 'Köpfe',
)
```

### Дивіться також

-   [Константы](class.collator.html#intl.collator-constants) [Collator](class.collator.html)
-   [collator\_sort()](collator.sort.html) - Сортує масив із використанням зазначеного засобу сортування
-   [collator\_asort()](collator.asort.html) - Сортує масив із збереженням асоціації індексу