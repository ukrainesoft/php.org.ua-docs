---
navigation:
  - class.collator.md: « Collator
  - collator.compare.md: 'Collator::compare »'
  - index.md: PHP Manual
  - class.collator.md: Collator
title: 'Collator::asort'
---
# Collator::asort

# collatorasort

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Collator::asort -- collatorasort — Сортує масив із збереженням асоціації індексу

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public Collator::asort(array &$array, int $flags = Collator::SORT_REGULAR): bool
```

Процедурний стиль

```methodsynopsis
collator_asort(Collator $object, array &$array, int $flags = Collator::SORT_REGULAR): bool
```

Функція сортує масив таким чином, щоб індекси масиву зберігали кореляцію з елементами масиву, з якими вони пов'язані. Це використовується в основному при сортуванні асоціативних масивів, де важливим є фактичний порядок елементів. Елементи масиву матимуть порядок сортування відповідно до поточних правил локалі.

Еквівалентно стандартної функції PHP [asort()](function.asort.md)

### Список параметрів

`object`

Об'єкт [Collator](class.collator.md)

`array`

Масив рядків для сортування.

`flags`

Необов'язковий тип сортування, один із таких:

-   **`Collator::SORT_REGULAR`** - порівнює елементи як завжди (не змінюючи тип)
    
-   **`Collator::SORT_NUMERIC`** - порівнює елементи, як числа
    
-   **`Collator::SORT_STRING`** - Порівнює елементи, як рядки
    

Значення `flags` за замовчуванням - **`Collator::SORT_REGULAR`**. Також використовується, якщо вказано неприпустиме значення `flags`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **collatorasort()****

```php
<?php
$coll = collator_create( 'en_US' );
$arr = array(
     'a' => '100',
     'b' => '50',
     'c' => '7'
);
collator_asort( $coll, $arr, Collator::SORT_NUMERIC );
var_export( $arr );

collator_asort( $coll, $arr, Collator::SORT_STRING );
var_export( $arr );
?>
```

Результат виконання цього прикладу:

```
array (
  'c' => '7',
  'b' => '50',
  'a' => '100',
)array (
  'a' => '100',
  'b' => '50',
  'c' => '7',
)
```

### Дивіться також

-   [Константи](class.collator.md#intl.collator-constants) [Collator](class.collator.md)
-   [collatorsort()](collator.sort.md) - Сортує масив із використанням зазначеного засобу сортування
-   [collatorsortwithsortkeys()](collator.sortwithsortkeys.md) - Сортує масив з використанням зазначеного Collator та ключів сортування
