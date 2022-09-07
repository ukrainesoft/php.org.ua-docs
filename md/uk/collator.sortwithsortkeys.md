---
navigation:
  - collator.setstrength.md: '« Collator::setStrength'
  - collator.sort.md: 'Collator::sort »'
  - index.md: PHP Manual
  - class.collator.md: Collator
title: 'Collator::sortWithSortKeys'
---
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

Те саме, що і [collatorsort()](collator.sort.md), але використовує ключі сортування ICU, створені ucolgetSortKey() збільшення швидкості роботи з великими масивами.

### Список параметрів

`object`

Об'єкт [Collator](class.collator.md)

`array`

Масив рядків для сортування

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **collatorsortwithsortkeys()****

```php
<?php
$arr  = array( 'Köpfe', 'Kypper', 'Kopfe' );
$coll = collator_create( 'sv' );

collator_sort_with_sort_keys( $coll, $arr );
var_export( $arr );
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

-   [Константи](class.collator.md#intl.collator-constants) [Collator](class.collator.md)
-   [collatorsort()](collator.sort.md) - Сортує масив із використанням зазначеного засобу сортування
-   [collatorasort()](collator.asort.md) - Сортує масив із збереженням асоціації індексу
