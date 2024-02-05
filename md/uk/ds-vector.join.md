---
navigation:
  - ds-vector.isempty.md: '« Ds\\Vector::isEmpty'
  - ds-vector.jsonserialize.md: 'Ds\\Vector::jsonSerialize »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::join'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::join

(PECL ds >= 1.0.0)

Ds\\Vector::join — Склеює всі значення в рядок

### Опис

```methodsynopsis
public Ds\Vector::join(string $glue = ?): string
```

Склеює всі значення у рядок, опціонально використовуючи заданий роздільник.

### Список параметрів

`glue`

Необов'язковий параметр, який визначає роздільник між значеннями.

### Значення, що повертаються

Всі значення вектора склеєні в один рядок.

### Приклади

**Пример #1 Пример использования**Ds\\Vector::join()\*\* з роздільником\*\*

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c", 1, 2, 3]);

var_dump($vector->join("|"));
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(11) "a|b|c|1|2|3"
```

**Пример #2 Пример использования**Ds\\Vector::join()\*\* без роздільника\*\*

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c", 1, 2, 3]);

var_dump($vector->join());
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(11) "abc123"
```
