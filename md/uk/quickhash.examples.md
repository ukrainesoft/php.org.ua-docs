---
navigation:
  - quickhash.constants.md: « Обумовлені константи
  - class.quickhashintset.md: QuickHashIntSet »
  - index.md: PHP Manual
  - book.quickhash.md: Quickhash
title: Приклади
---
# Приклади

**Приклад #1 Приклад використання Quickhash**

```php
<?php
$set = new QuickHashIntSet( 1024, QuickHashIntSet::CHECK_FOR_DUPES );
$set->add( 1 );
$set->add( 3 );

var_dump( $set->exists( 3 ) );
var_dump( $set->exists( 4 ) );

$set->saveToFile( "/tmp/test-set.set" );

$newSet = QuickHashIntSet::loadFromFile(
    "/tmp/test-set.set"
);

var_dump( $newSet->exists( 3 ) );
var_dump( $newSet->exists( 4 ) );
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
bool(false)
bool(true)
bool(false)
```

**Приклад #2 Приклад використання Quickhash ArrayAccess**

```php
<?php
$hash = new QuickHashIntHash( 64 );

// Добавление и обновление записей хеша.
$hash[3] = 145926;
$hash[3] = 1415926;
$hash[2] = 72;

// Проверка существования ключей
var_dump( isset( $hash[3] ) );

// Удаление записей хеша
unset( $hash[2] );

// Получение значения, сохранённого для хеша
echo $hash[3], "\n";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
1415926
```

**Приклад #3 Приклад використання Quickhash Iterator**

```php
<?php
$hash = new QuickHashIntHash( 64 );

// Добавление записей хеша.
$hash[1] = 145926;
$hash[2] = 1415926;
$hash[3] = 72;
$hash[4] = 712314;
$hash[5] = -4234;

foreach( $hash as $key => $value )
{
    echo $key, ' => ', $value, "\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
5 => -4234
4 => 712314
1 => 145926
2 => 1415926
3 => 72
```

**Приклад #4 Приклад використання Quickhash String Values**

```php
<?php
$hash = new QuickHashIntStringHash( 64 );

// Добавление записей хеша.
$hash[1] = "один миллион четыреста пятнадцать тысяч девятьсот двадцать шесть";
$hash->add( 2, "ещё один" );

foreach( $hash as $key => $value )
{
    echo $key, ' => ', $value, "\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
1 => один миллион четыреста пятнадцать тысяч девятьсот двадцать шесть
2 => ещё один
```
