---
navigation:
  - ds-set.reduce.md: '« Ds\\Set::reduce'
  - ds-set.reverse.md: 'Ds\\Set::reverse »'
  - index.md: PHP Manual
  - class.ds-set.md: Ds\\Set
title: 'Ds\\Set::remove'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Set::remove

(PECL ds >= 1.0.0)

Ds\\Set::remove — Видалення всіх заданих значень з набору

### Опис

```methodsynopsis
public Ds\Set::remove(mixed ...$values): void
```

Видаляє всі задані значення `values` з набору. Значення, які відсутні в наборі, будуть проігноровані.

### Список параметрів

`values`

Значення видалення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**Ds\\Set::remove()\*\*\*\*

```php
<?php
$set = new \Ds\Set([1, 2, 3, 4, 5]);

$set->remove(1);            // Удалить 1
$set->remove(1, 2);         // Невозможно найти 1, но удалить 2
$set->remove(...[3, 4]);    // Удалить 3 и 4

var_dump($set);
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(Ds\Set)#1 (1) {
  [0]=>
  int(5)
}
```
