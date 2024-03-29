---
navigation:
  - splobjectstorage.detach.md: '« SplObjectStorage::detach'
  - splobjectstorage.getinfo.md: 'SplObjectStorage::getInfo »'
  - index.md: PHP Manual
  - class.splobjectstorage.md: SplObjectStorage
title: 'SplObjectStorage::getHash'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplObjectStorage::getHash

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

SplObjectStorage::getHash — Обчислює унікальний ідентифікатор об'єктів контейнера

### Опис

```methodsynopsis
public SplObjectStorage::getHash(object $object): string
```

Метод обчислює унікальний ідентифікатор для об'єктів, що додаються до контейнера [SplObjectStorage](class.splobjectstorage.md)

Реализация[SplObjectStorage](class.splobjectstorage.md) повертає те саме значення, що і функція [spl\_object\_hash()](function.spl-object-hash.md)

В одному контейнері ніколи не з'явиться два об'єкти з однаковими ідентифікаторами. Таким чином, за допомогою контейнера можна реалізувати безліч (колекцію значень, кожне з яких представлено в єдиному екземплярі), в якому унікальність об'єктів визначатиметься цим ідентифікатором.

### Список параметрів

`object`

Об'єкт, ідентифікатор якого потрібно обчислити.

### Значення, що повертаються

Рядок string з результатом обчислення.

### Помилки

Метод викидає виняток [RuntimeException](class.runtimeexception.md), коли тип значення, що повертається не є рядком (string).

### Приклади

**Приклад #1 Приклад використання** SplObjectStorage::getHash()\*\*\*\*

```php
<?php
class OneSpecimenPerClassStorage extends SplObjectStorage {
    public function getHash($o) {
        return get_class($o);
    }
}
class A {}

$s = new OneSpecimenPerClassStorage;
$o1 = new stdClass;
$o2 = new stdClass;
$o3 = new A;

$s[$o1] = 1;
//$o2 предполагается равным $o1, соответственно значение замещается
$s[$o2] = 2;
$s[$o3] = 3;

//предполагаем, что следующие объекты эквивалентны приведённым выше
//таким образом, их можно использовать для извлечения данных из контейнера
$p1 = new stdClass;
$p2 = new A;
echo $s[$p1], "\n";
echo $s[$p2], "\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
2
3
```

### Дивіться також

-   [spl\_object\_hash()](function.spl-object-hash.md) \- Повертає хеш-ідентифікатор для об'єкта
