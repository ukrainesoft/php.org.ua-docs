---
navigation:
  - multipleiterator.attachiterator.md: '« MultipleIterator::attachIterator'
  - multipleiterator.containsiterator.md: 'MultipleIterator::containsIterator »'
  - index.md: PHP Manual
  - class.multipleiterator.md: MultipleIterator
title: 'MultipleIterator::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MultipleIterator::\_\_construct

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

MultipleIterator::\_\_construct — Створює новий MultipleIterator

### Опис

public **MultipleIterator::\_\_construct**(int`$flags`\= MultipleIterator::MIT\_NEED\_ALL | MultipleIterator::MIT\_KEYS\_NUMERIC)

Створює новий MultipleIterator.

### Список параметрів

`flags`

Флаги для установки, согласно[Обумовленим константам](class.multipleiterator.md#multipleiterator.constants)

-   **`MultipleIterator::MIT_NEED_ALL`** або **`MultipleIterator::MIT_NEED_ANY`**
-   **`MultipleIterator::MIT_KEYS_NUMERIC`** або **`MultipleIterator::MIT_KEYS_ASSOC`**

По умолчанию\*\*`MultipleIterator::MIT_NEED_ALL`\*\* **`MultipleIterator::MIT_KEYS_NUMERIC`**

### Приклади

**Приклад #1 Ітерування MultipleIterator**

```php
<?php
$people = new ArrayIterator(array('John', 'Jane', 'Jack', 'Judy'));
$roles  = new ArrayIterator(array('Developer', 'Scrum Master', 'Project Owner'));

$team = new MultipleIterator($flags);
$team->attachIterator($people, 'person');
$team->attachIterator($roles, 'role');

foreach ($team as $member) {
    print_r($member);
}
?>
```

Висновок з `$flags = MIT_NEED_ALL|MIT_KEYS_NUMERIC`

```
Array
(
    [0] => John
    [1] => Developer
)
Array
(
    [0] => Jane
    [1] => Scrum Master
)
Array
(
    [0] => Jack
    [1] => Project Owner
)
```

Висновок з `$flags = MIT_NEED_ANY|MIT_KEYS_NUMERIC`

```
Array
(
    [0] => John
    [1] => Developer
)
Array
(
    [0] => Jane
    [1] => Scrum Master
)
Array
(
    [0] => Jack
    [1] => Project Owner
)
Array
(
    [0] => Judy
    [1] =>
)
```

Висновок з `$flags = MIT_NEED_ALL|MIT_KEYS_ASSOC`

```
Array
(
    [person] => John
    [role] => Developer
)
Array
(
    [person] => Jane
    [role] => Scrum Master
)
Array
(
    [person] => Jack
    [role] => Project Owner
)
```

Висновок з `$flags = MIT_NEED_ANY|MIT_KEYS_ASSOC`

```
Array
(
    [person] => John
    [role] => Developer
)
Array
(
    [person] => Jane
    [role] => Scrum Master
)
Array
(
    [person] => Jack
    [role] => Project Owner
)
Array
(
    [person] => Judy
    [role] =>
)
```

### Дивіться також

-   [Обумовлені константи](class.multipleiterator.md#multipleiterator.constants)
-   [MultipleIterator::valid()](multipleiterator.valid.md) \- Перевіряє коректність підитераторів
