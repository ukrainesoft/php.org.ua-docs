---
navigation:
  - spl.misc.md: « Різні класи та інтерфейси
  - arrayobject.append.md: 'ArrayObject::append »'
  - index.md: PHP Manual
  - spl.misc.md: Різні класи та інтерфейси
title: Клас ArrayObject
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас ArrayObject

(PHP 5, PHP 7, PHP 8)

## Вступ

Цей клас дозволяє об'єктам працювати як масиви.

## Огляд класів

```classsynopsis

    
     class ArrayObject
    

    
     implements
      IteratorAggregate,

     ArrayAccess,

     Serializable,

     Countable {

    /* Константы */
    
     const
     int
      STD_PROP_LIST;

    const
     int
      ARRAY_AS_PROPS;


    /* Методы */
    
   public __construct(array|object $array = [], int $flags = 0, string $iteratorClass = ArrayIterator::class)

    public append(mixed $value): void
public asort(int $flags = SORT_REGULAR): true
public count(): int
public exchangeArray(array|object $array): array
public getArrayCopy(): array
public getFlags(): int
public getIterator(): Iterator
public getIteratorClass(): string
public ksort(int $flags = SORT_REGULAR): true
public natcasesort(): true
public natsort(): true
public offsetExists(mixed $key): bool
public offsetGet(mixed $key): mixed
public offsetSet(mixed $key, mixed $value): void
public offsetUnset(mixed $key): void
public serialize(): string
public setFlags(int $flags): void
public setIteratorClass(string $iteratorClass): void
public uasort(callable $callback): true
public uksort(callable $callback): true
public unserialize(string $data): void

   }
```

## Обумовлені константи

## Опції ArrayObject

**`ArrayObject::STD_PROP_LIST`**

Властивості об'єкта поводяться як завжди при доступі до них як до елементів списку ([var\_dump()](function.var-dump.md) [foreach](control-structures.foreach.md)и т. д.).

**`ArrayObject::ARRAY_AS_PROPS`**

Доступ до елементів можна отримати як до властивостей об'єкта (для читання та запису).

## Зміст

-   [ArrayObject::append](arrayobject.append.md)— Додає значення до кінця масиву
-   [ArrayObject::asort](arrayobject.asort.md)— Сортувати записи за значенням
-   [ArrayObject::\_\_construct](arrayobject.construct.md)— Створює новий об'єкт масиву
-   [ArrayObject::count](arrayobject.count.md)— Отримати кількість загальнодоступних властивостей ArrayObject
-   [ArrayObject::exchangeArray](arrayobject.exchangearray.md) \- Замінити масив на інший
-   [ArrayObject::getArrayCopy](arrayobject.getarraycopy.md) \- Створює копію ArrayObject
-   [ArrayObject::getFlags](arrayobject.getflags.md)— Отримує прапори поведінки
-   [ArrayObject::getIterator](arrayobject.getiterator.md)— Створити новий ітератор із екземпляра ArrayObject
-   [ArrayObject::getIteratorClass](arrayobject.getiteratorclass.md)— Отримує ім'я класу ітератора для ArrayObject
-   [ArrayObject::ksort](arrayobject.ksort.md)— Сортувати записи за ключами
-   [ArrayObject::natcasesort](arrayobject.natcasesort.md) - Сортувати масив, використовуючи реєстронезалежний алгоритм "natural order"
-   [ArrayObject::natsort](arrayobject.natsort.md) - Сортувати масив, використовуючи алгоритм "natural order"
-   [ArrayObject::offsetExists](arrayobject.offsetexists.md)— Повертає, чи вказаний індекс існує
-   [ArrayObject::offsetGet](arrayobject.offsetget.md)— Повертає значення за вказаним індексом
-   [ArrayObject::offsetSet](arrayobject.offsetset.md)— Встановлює нове значення за вказаним індексом
-   [ArrayObject::offsetUnset](arrayobject.offsetunset.md)— Видаляє значення за вказаним індексом
-   [ArrayObject::serialize](arrayobject.serialize.md) \- Серіалізувати ArrayObject
-   [ArrayObject::setFlags](arrayobject.setflags.md) \- Встановлює прапори поведінки
-   [ArrayObject::setIteratorClass](arrayobject.setiteratorclass.md)— Встановлює ім'я класу ітератора ArrayObject
-   [ArrayObject::uasort](arrayobject.uasort.md)— Сортувати записи, використовуючи функцію користувача для порівняння елементів і зберігаючи при цьому зв'язок ключ/значення
-   [ArrayObject::uksort](arrayobject.uksort.md)— Сортувати масив за ключами, використовуючи функцію користувача для порівняння
-   [ArrayObject::unserialize](arrayobject.unserialize.md) \- Десеріалізувати ArrayObject
