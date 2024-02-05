---
navigation:
  - ds-deque.isempty.md: '« Ds\\Deque::isEmpty'
  - ds-deque.jsonserialize.md: 'Ds\\Deque::jsonSerialize »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::join'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::join

(PECL ds >= 1.0.0)

Ds\\Deque::join — Склеює всі значення в рядок

### Опис

```methodsynopsis
public Ds\Deque::join(string $glue = ?): string
```

Склеює всі значення у рядок, опціонально використовуючи заданий роздільник.

### Список параметрів

`glue`

Необов'язковий параметр, який визначає роздільник між значеннями.

### Значення, що повертаються

Усі значення колекції склеєні в один рядок.

### Приклади

**Приклад #1 Приклад використання** Ds\\Deque::join()\*\* з роздільником\*\*

```php
<?php
$deque = new \Ds\Deque(["a", "b", "c", 1, 2, 3]);

var_dump($deque->join("|"));
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(11) "a|b|c|1|2|3"
```

**Приклад #2 Приклад використання** Ds\\Deque::join()\*\* без роздільника\*\*

```php
<?php
$deque = new \Ds\Deque(["a", "b", "c", 1, 2, 3]);

var_dump($deque->join());
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(11) "abc123"
```
