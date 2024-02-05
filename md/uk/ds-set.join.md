---
navigation:
  - ds-set.isempty.md: '« Ds\\Set::isEmpty'
  - ds-set.jsonserialize.md: 'Ds\\Set::jsonSerialize »'
  - index.md: PHP Manual
  - class.ds-set.md: Ds\\Set
title: 'Ds\\Set::join'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Set::join

(PECL ds >= 1.0.0)

Ds\\Set::join — Склеює всі значення в рядок

### Опис

```methodsynopsis
public Ds\Set::join(string $glue = ?): string
```

Склеює всі значення у рядок, опціонально використовуючи заданий роздільник.

### Список параметрів

`glue`

Необов'язковий параметр, який визначає роздільник між значеннями.

### Значення, що повертаються

Усі значення колекції склеєні в один рядок.

### Приклади

**Пример #1 Пример использования**Ds\\Set::join()\*\* з роздільником\*\*

```php
<?php
$set = new \Ds\Set(["a", "b", "c", 1, 2, 3]);

var_dump($set->join("|"));
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(11) "a|b|c|1|2|3"
```

**Пример #2 Пример использования**Ds\\Set::join()\*\* без роздільника\*\*

```php
<?php
$set = new \Ds\Set(["a", "b", "c", 1, 2, 3]);

var_dump($set->join());
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(11) "abc123"
```
