Перетворює пару на масив (array)

-   [« Ds\\Pair::jsonSerialize](ds-pair.jsonserialize.html)
    
-   [Набор »](class.ds-set.html)
    
-   [PHP Manual](index.html)
    
-   [Пара](class.ds-pair.html)
    
-   Перетворює пару на масив (array)
    

# ДсPair::toArray

(PECL ds >= 1.0.0)

ДсPair::toArray - Перетворює пару в масив (array)

### Опис

```methodsynopsis
public Ds\Pair::toArray(): array
```

Перетворює пару на масив (array).

> **Зауваження**
> 
> Приведення до масиву поки що не підтримується.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив містить елементи в тому ж порядку, як вони були в парі.

### Приклади

**Приклад #1 Приклад використання **ДсPair::toArray()****

```php
<?php
$pair = new \Ds\Pair("a", 1);

var_dump($pair->toArray());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(2) {
  ["key"]=>
  string(1) "a"
  ["value"]=>
  int(1)
}
```