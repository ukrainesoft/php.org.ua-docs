---
navigation:
  - ds-set.construct.md: '« Ds\\Set::\_\_construct'
  - ds-set.copy.md: 'Ds\\Set::copy »'
  - index.md: PHP Manual
  - class.ds-set.md: Ds\\Set
title: 'Ds\\Set::contains'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Set::contains

(PECL ds >= 1.0.0)

Ds\\Set::contains — Перевіряє, чи в колекції задані значення

### Опис

```methodsynopsis
public Ds\Set::contains(mixed ...$values): bool
```

Перевіряє, чи міститься у колекції задані значення.

> **Зауваження** :
> 
> Підтримуються значення типу об'єкта. Якщо об'єкт реалізує інтерфейс [Ds\\Hashable](class.ds-hashable.md), перевірка здійснюється шляхом виклику методу об'єкта `equals`. Якщо об'єкт не реалізує інтерфейс [Ds\\Hashable](class.ds-hashable.md), об'єкти повинні посилатися на той самий екземпляр класу.

**Застереження**

Усі порівняння суворі, за типом та значенням.

### Список параметрів

`values`

Значення для перевірки.

### Значення, що повертаються

Повертає \*\*`false`\*\*якщо хоча б одне значення з `values` не знайдено в колекції та **`true`** в іншому випадку.

### Приклади

**Пример #1 Пример использования**Ds\\Set::contains()\*\*\*\*

```php
<?php
$set = new \Ds\Set([1, 2, 3]);

var_dump($set->contains(1));                // true
var_dump($set->contains(1, 2));             // true
var_dump($set->contains(...[1, 2]));        // true

var_dump($set->contains("1"));              // false
var_dump($set->contains(...[1, 2, 3, 4]));  // false

var_dump($set->contains(...[]));            // true
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
bool(true)
bool(true)
bool(false)
bool(false)
bool(true)
```
