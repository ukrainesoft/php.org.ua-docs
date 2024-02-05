---
navigation:
  - ds-sequence.insert.md: '« Ds\\Sequence::insert'
  - ds-sequence.last.md: 'Ds\\Sequence::last »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::join'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::join

(PECL ds >= 1.0.0)

Ds\\Sequence::join — Склеює всі значення в рядок

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

**Пример #1 Пример использования**Ds\\Sequence::join()\*\* з роздільником\*\*

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c", 1, 2, 3]);

var_dump($sequence->join("|"));
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(11) "a|b|c|1|2|3"
```

**Пример #2 Пример использования**Ds\\Sequence::join()\*\* без роздільника\*\*

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c", 1, 2, 3]);

var_dump($sequence->join());
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(11) "abc123"
```
