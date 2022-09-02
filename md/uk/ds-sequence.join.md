---
navigation:
  - ds-sequence.insert.md: '« DsSequence::insert'
  - ds-sequence.last.md: 'ДсSequence::last »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Послідовність
title: 'ДсSequence::join'
---
# ДсSequence::join

(PECL ds >= 1.0.0)

ДсSequence::join — Склеює всі значення в рядок

### Опис

```methodsynopsis
abstract public Ds\Sequence::join(string $glue = ?): string
```

Склеює всі значення у рядок, опціонально використовуючи заданий роздільник.

### Список параметрів

`glue`

Необов'язковий параметр, який визначає роздільник між значеннями.

### Значення, що повертаються

Усі значення колекції склеєні в один рядок.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::join()** з роздільником**

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c", 1, 2, 3]);

var_dump($sequence->join("|"));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(11) "a|b|c|1|2|3"
```

**Приклад #2 Приклад використання **ДсSequence::join()** без роздільника**

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c", 1, 2, 3]);

var_dump($sequence->join());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(11) "abc123"
```
