---
navigation:
  - collator.asort.md: '« Collator::asort'
  - collator.construct.md: 'Collator::\_\_construct »'
  - index.md: PHP Manual
  - class.collator.md: Collator
title: 'Collator::compare'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Collator::compare

# collator\_compare

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Collator::compare -- collator\_compare — Порівнює два рядки Unicode

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public Collator::compare(string $string1, string $string2): int|false
```

Процедурний стиль

```methodsynopsis
collator_compare(Collator $object, string $string1, string $string2): int|false
```

Порівнює два рядки Unicode відповідно до правил зіставлення.

### Список параметрів

`object`

Об'єкт [Collator](class.collator.md)

`string1`

Перший рядок для порівняння.

`string2`

Другий рядок для порівняння.

### Значення, що повертаються

Повертає результат порівняння:

-   1, якщо`string1` *більше* `string2`
    
-   0, якщо`string1` *дорівнює* `string2`
    
-   \-1, якщо`string1` *менше* `string2`
    

У разі виникнення помилки повертає **`false`**

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Логічний тип](language.types.boolean.md)Используйте[оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### Приклади

**Приклад #1 Приклад використання** collator\_compare()\*\*\*\*

```php
<?php
$s1 = 'Hello';
$s2 = 'hello';

$coll = collator_create( 'en_US' );
$res  = collator_compare( $coll, $s1, $s2 );

if ($res === false) {
    echo collator_get_error_message( $coll );
} else if( $res > 0 ) {
    echo "s1 больше s2\n";
} else if( $res < 0 ) {
    echo "s1 меньше s2\n";
} else {
    echo "s1 и s2 равны\n";
}
?>
```

Результат виконання наведеного прикладу:

s1 больше s2

**Приклад #2 Порівняння рядків без діакритичних знаків та без урахування регістру**

```php
<?php
$c = new Collator( 'en' );
$c->setStrength( Collator::PRIMARY );

if ( $c->compare( 'Séan', 'Sean' ) == 0 )
{
    echo "Значения равны\n";
}
```

Результат виконання наведеного прикладу:

Значення рівні

У цьому прикладі Collator порівнює, враховуючи лише базові символи. Документація для [Collator->setStrength()](collator.setstrength.md) пояснює різні сильні сторони.

### Дивіться також

-   [collator\_sort()](collator.sort.md) \- Сортує масив із використанням зазначеного засобу сортування
