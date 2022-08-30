Перевіряє, чи міститься в колекції задані значення

-   [« DsSet::construct](ds-set.construct.html)
    
-   [ДсSet::copy »](ds-set.copy.html)
    
-   [PHP Manual](index.html)
    
-   [Набор](class.ds-set.html)
    
-   Перевіряє, чи міститься в колекції задані значення
    

# ДсSet::contains

(PECL ds >= 1.0.0)

ДсSet::contains — Перевіряє, чи в колекції задані значення

### Опис

```methodsynopsis
public Ds\Set::contains(mixed ...$values): bool
```

Перевіряє, чи міститься у колекції задані значення.

> **Зауваження**
> 
> Підтримуються значення типу об'єкта. Якщо об'єкт реалізує інтерфейс **ДсHashable**, перевірка здійснюється шляхом виклику методу об'єкта `equals`. Якщо об'єкт не реалізує інтерфейс **ДсHashable**, об'єкти повинні посилатися на той самий екземпляр класу.

**Застереження**

Усі порівняння суворі, за типом та значенням.

### Список параметрів

`values`

Значення для перевірки.

### Значення, що повертаються

Повертає \*\*`false`\*\*якщо хоча б одне значення з `values` не знайдено в колекції та **`true`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ДсSet::contains()****

```php
<?php
$set = new \Ds\Set([1, 2, 3]);

var_dump($set->contains(1));                // true
var_dump($set->contains(1, 2));             // true
var_dump($set->contains(...[1, 2]));        // true

var_dump($set->contains("1"));              // false
var_dump($set->contains(...[1, 2, 3, 4]));  // false

var_dump($set->contains(...[]));            // true
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
bool(true)
bool(true)
bool(false)
bool(false)
bool(true)
```