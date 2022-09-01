---
navigation:
  - spl.misc.html: « Різні класи та інтерфейси
  - arrayobject.append.html: 'ArrayObject::append »'
  - index.html: PHP Manual
  - spl.misc.html: Різні класи та інтерфейси
title: Клас ArrayObject
---
# Клас ArrayObject

(PHP 5, PHP 7, PHP 8)

## Вступ

Цей клас дозволяє об'єктам працювати як масиви.

## Огляд класів

```classsynopsis

     
    

    
     
      class ArrayObject
     

     implements 
       IteratorAggregate,  ArrayAccess,  Serializable,  Countable {

    /* Константы */
    
     const
     int
      STD_PROP_LIST = 1;

    const
     int
      ARRAY_AS_PROPS = 2;


    /* Методы */
    
   public __construct(array|object $array = [], int $flags = 0, string $iteratorClass = ArrayIterator::class)

    public append(mixed $value): void
public asort(int $flags = SORT_REGULAR): bool
public count(): int
public exchangeArray(array|object $array): array
public getArrayCopy(): array
public getFlags(): int
public getIterator(): Iterator
public getIteratorClass(): string
public ksort(int $flags = SORT_REGULAR): bool
public natcasesort(): bool
public natsort(): bool
public offsetExists(mixed $key): bool
public offsetGet(mixed $key): mixed
public offsetSet(mixed $key, mixed $value): void
public offsetUnset(mixed $key): void
public serialize(): string
public setFlags(int $flags): void
public setIteratorClass(string $iteratorClass): void
public uasort(callable $callback): bool
public uksort(callable $callback): bool
public unserialize(string $data): void

   }
```

## Обумовлені константи

## Опції ArrayObject

**`ArrayObject::STD_PROP_LIST`**

Властивості об'єкта набувають стандартної поведінки при доступі у вигляді списку (vardump, foreach і т.д.).

**`ArrayObject::ARRAY_AS_PROPS`**

Записи можуть бути доступні як властивості (для читання та запису).

## Зміст

-   [ArrayObject::append](arrayobject.append.html) — Додає значення до кінця масиву
-   [ArrayObject::asort](arrayobject.asort.html) — Сортувати записи за значенням
-   [ArrayObject::construct](arrayobject.construct.html) — Створює новий об'єкт масиву
-   [ArrayObject::count](arrayobject.count.html) — Отримати кількість загальнодоступних властивостей ArrayObject
-   [ArrayObject::exchangeArray](arrayobject.exchangearray.html) - Замінити масив на інший
-   [ArrayObject::getArrayCopy](arrayobject.getarraycopy.html) - Створює копію ArrayObject
-   [ArrayObject::getFlags](arrayobject.getflags.html) — Отримує прапори поведінки
-   [ArrayObject::getIterator](arrayobject.getiterator.html) — Створити новий ітератор із екземпляра ArrayObject
-   [ArrayObject::getIteratorClass](arrayobject.getiteratorclass.html) — Отримує ім'я класу ітератора для ArrayObject
-   [ArrayObject::ksort](arrayobject.ksort.html) — Сортувати записи за ключами
-   [ArrayObject::natcasesort](arrayobject.natcasesort.html) - Сортувати масив, використовуючи реєстронезалежний алгоритм "natural order"
-   [ArrayObject::natsort](arrayobject.natsort.html) - Сортувати масив, використовуючи алгоритм "natural order"
-   [ArrayObject::offsetExists](arrayobject.offsetexists.html) — Повертає, чи вказаний індекс існує
-   [ArrayObject::offsetGet](arrayobject.offsetget.html) — Повертає значення за вказаним індексом
-   [ArrayObject::offsetSet](arrayobject.offsetset.html) — Встановлює нове значення за вказаним індексом
-   [ArrayObject::offsetUnset](arrayobject.offsetunset.html) — Видаляє значення за вказаним індексом
-   [ArrayObject::serialize](arrayobject.serialize.html) - Серіалізувати ArrayObject
-   [ArrayObject::setFlags](arrayobject.setflags.html) - Встановлює прапори поведінки
-   [ArrayObject::setIteratorClass](arrayobject.setiteratorclass.html) — Встановлює ім'я класу ітератора ArrayObject
-   [ArrayObject::uasort](arrayobject.uasort.html) — Сортувати записи, використовуючи функцію користувача для порівняння елементів і зберігаючи при цьому зв'язок ключ/значення
-   [ArrayObject::uksort](arrayobject.uksort.html) — Сортувати масив за ключами, використовуючи функцію користувача для порівняння
-   [ArrayObject::unserialize](arrayobject.unserialize.html) - Десеріалізувати ArrayObject
