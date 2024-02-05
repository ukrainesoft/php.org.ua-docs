---
navigation:
  - ds-map.pairs.md: '« Ds\\Map::pairs'
  - ds-map.putall.md: 'Ds\\Map::putAll »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::put'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::put

(PECL ds >= 1.0.0)

Ds\\Map::put — Встановлення значення за заданим ключем

### Опис

```methodsynopsis
public Ds\Map::put(mixed $key, mixed $value): void
```

Зв'язує ключ `key`со значением`value`якщо елемент з таким ключем вже існує - його значення перезаписується.

> **Зауваження** :
> 
> Підтримуються значення типу об'єкта. Якщо об'єкт реалізує інтерфейс [Ds\\Hashable](class.ds-hashable.md), перевірка здійснюється шляхом виклику методу об'єкта `equals`. Якщо об'єкт не реалізує інтерфейс [Ds\\Hashable](class.ds-hashable.md), об'єкти повинні посилатися на той самий екземпляр класу.

> **Зауваження** :
> 
> Ви можете використовувати синтаксис масиву для доступу до значень, тобто . `$map["key"]`

**Застереження**

Будьте обережні під час використання синтаксису масиву. Скалярні ключі будуть приведені до всіх двигунів PHP. Наприклад, `$map["1"]` буде намагатися звернутися до `int(1)`, тогда как`$map->get("1")` звернеться до правильного елемента.

Смотрите раздел [Масиви](language.types.array.md)

### Список параметрів

`key`

Ключ.

`value`

значення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**Ds\\Map::put()\*\*\*\*

```php
<?php
$map = new \Ds\Map();

$map->put("a", 1);
$map->put("b", 2);
$map->put("c", 3);

print_r($map);
?>
```

Висновок наведеного прикладу буде схожим на:

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

**Пример #2 Пример использования**Ds\\Map::put()\*\* з об'єктами як ключі\*\*

```php
<?php
class HashableObject implements \Ds\Hashable
{
    /**
     * Значение, которое мы будем использовать в качестве хеша. Не определяет идентичность.
     */
    private $value;

    public function __construct($value)
    {
        $this->value = $value;
    }

    public function hash()
    {
        return $this->value;
    }

    public function equals($obj): bool
    {
        return $this->value === $obj->value;
    }
}

$map = new \Ds\Map();

$obj = new \ArrayIterator([]);

// Использование одного и того же экземпляра объекта несколько раз будет каждый раз
// перезаписывать значение
$map->put($obj, 1);
$map->put($obj, 2);

// Использование разных экземпляров одного и того же класса будет создавать новые
// элементы
$map->put(new \stdClass(), 3);
$map->put(new \stdClass(), 4);

// Использование одинаковых hashable-экземпляров несколько раз будет перезаписывать
// предыдущие значения
$map->put(new \HashableObject(1), 5);
$map->put(new \HashableObject(1), 6);
$map->put(new \HashableObject(2), 7);
$map->put(new \HashableObject(2), 8);

var_dump($map);
?>
```

Висновок наведеного прикладу буде схожим на:

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
