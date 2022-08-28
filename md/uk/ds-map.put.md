Встановлення значення за заданим ключем

-   [« Ds\\Map::pairs](ds-map.pairs.html)
    
-   [Ds\\Map::putAll »](ds-map.putall.html)
    
-   [PHP Manual](index.html)
    
-   [Коллекция пар ключ-значение](class.ds-map.html)
    
-   Встановлення значення за заданим ключем
    

# ДсMap::put

(PECL ds >= 1.0.0)

ДсMap::put — Встановлення значення за заданим ключем

### Опис

```methodsynopsis
public Ds\Map::put(mixed $key, mixed $value): void
```

Зв'язує ключ `key` зі значенням `value`якщо елемент з таким ключем вже існує - його значення перезаписується.

> **Зауваження**
> 
> Підтримуються значення типу об'єкта. Якщо об'єкт реалізує інтерфейс **ДсHashable**, перевірка здійснюється шляхом виклику методу об'єкта `equals`. Якщо об'єкт не реалізує інтерфейс **ДсHashable**, об'єкти повинні посилатися на той самий екземпляр класу.

> **Зауваження**
> 
> Ви можете використовувати синтаксис масиву для доступу до значень, тобто . `$map["key"]`

**Застереження**

Будьте обережні під час використання синтаксису масиву. Скалярні ключі будуть приведені до всіх двигунів PHP. Наприклад, `$map["1"]` буде намагатися звернутися до `int(1)`, тоді як `$map->get("1")` звернеться до правильного елемента.

Дивіться розділ [Массивы](language.types.array.html)

### Список параметрів

`key`

Ключ.

`value`

значення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсMap::put()****

```php
<?php
$map = new \Ds\Map();

$map->put("a", 1);
$map->put("b", 2);
$map->put("c", 3);

print_r($map);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => a
            [value] => 1
        )

    [1] => Ds\Pair Object
        (
            [key] => b
            [value] => 2
        )

    [2] => Ds\Pair Object
        (
            [key] => c
            [value] => 3
        )

)
```

**Приклад #2 Приклад використання **ДсMap::put()** з об'єктами як ключі**

```php
<?php
class HashableObject implements \Ds\Hashable
{
    /**
     * Значение, которое мы будем использовать в качестве хеша. Не определяет идентичность.
     */
    private $value;

    public function __construct($value)
    {
        $this->value = $value;
    }

    public function hash()
    {
        return $this->value;
    }

    public function equals($obj): bool
    {
        return $this->value === $obj->value;
    }
}

$map = new \Ds\Map();

$obj = new \ArrayIterator([]);

// Использование одного и того же экземпляра объекта несколько раз будет каждый раз
// перезаписывать значение
$map->put($obj, 1);
$map->put($obj, 2);

// Использование разных экземпляров одного и того же класса будет создавать новые
// элементы
$map->put(new \stdClass(), 3);
$map->put(new \stdClass(), 4);

// Использование одинаковых hashable-экземпляров несколько раз будет перезаписывать
// предыдущие значения
$map->put(new \HashableObject(1), 5);
$map->put(new \HashableObject(1), 6);
$map->put(new \HashableObject(2), 7);
$map->put(new \HashableObject(2), 8);

var_dump($map);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Map)#1 (5) {
  [0]=>
  object(Ds\Pair)#7 (2) {
    ["key"]=>
    object(ArrayIterator)#2 (1) {
      ["storage":"ArrayIterator":private]=>
      array(0) {
      }
    }
    ["value"]=>
    int(2)
  }
  [1]=>
  object(Ds\Pair)#8 (2) {
    ["key"]=>
    object(stdClass)#3 (0) {
    }
    ["value"]=>
    int(3)
  }
  [2]=>
  object(Ds\Pair)#9 (2) {
    ["key"]=>
    object(stdClass)#4 (0) {
    }
    ["value"]=>
    int(4)
  }
  [3]=>
  object(Ds\Pair)#10 (2) {
    ["key"]=>
    object(HashableObject)#5 (1) {
      ["value":"HashableObject":private]=>
      int(1)
    }
    ["value"]=>
    int(6)
  }
  [4]=>
  object(Ds\Pair)#11 (2) {
    ["key"]=>
    object(HashableObject)#6 (1) {
      ["value":"HashableObject":private]=>
      int(2)
    }
    ["value"]=>
    int(8)
  }
}
```