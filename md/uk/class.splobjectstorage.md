---
navigation:
  - splfixedarray.wakeup.md: '« SplFixedArray::\_\_wakeup'
  - splobjectstorage.addall.md: 'SplObjectStorage::addAll »'
  - index.md: PHP Manual
  - spl.datastructures.md: Структури даних
title: Клас SplObjectStorage
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SplObjectStorage

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

## Вступ

Клас SplObjectStorage надає відображення об'єктів даних або набір об'єктів, ігноруючи дані. Ця подвійна мета може бути корисною у багатьох випадках, включаючи необхідність унікальної ідентифікації об'єктів.

## Огляд класів

```classsynopsis

    
     class SplObjectStorage
    

    
     implements
      Countable,

     Iterator,

     Serializable,

     ArrayAccess {

    /* Методы */
    
   public addAll(SplObjectStorage $storage): int
public attach(object $object, mixed $info = null): void
public contains(object $object): bool
public count(int $mode = COUNT_NORMAL): int
public current(): object
public detach(object $object): void
public getHash(object $object): string
public getInfo(): mixed
public key(): int
public next(): void
public offsetExists(object $object): bool
public offsetGet(object $object): mixed
public offsetSet(object $object, mixed $info = null): void
public offsetUnset(object $object): void
public removeAll(SplObjectStorage $storage): int
public removeAllExcept(SplObjectStorage $storage): int
public rewind(): void
public serialize(): string
public setInfo(mixed $info): void
public unserialize(string $data): void
public valid(): bool

   }
```

## Приклади

**Пример #1 Класс**SplObjectStorage\*\* як набір об'єктів\*\*

```php
<?php
// Набор объектов
$s = new SplObjectStorage();

$o1 = new stdClass;
$o2 = new stdClass;
$o3 = new stdClass;

$s->attach($o1);
$s->attach($o2);

var_dump($s->contains($o1));
var_dump($s->contains($o2));
var_dump($s->contains($o3));

$s->detach($o2);

var_dump($s->contains($o1));
var_dump($s->contains($o2));
var_dump($s->contains($o3));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(true)
bool(false)
bool(true)
bool(false)
bool(false)
```

**Пример #2 Класс**SplObjectStorage\*\* як відображення об'єктів у дані\*\*

```php
<?php
// Как отображение объектов к данным
$s = new SplObjectStorage();

$o1 = new stdClass;
$o2 = new stdClass;
$o3 = new stdClass;

$s[$o1] = "данные для объекта 1";
$s[$o2] = array(1,2,3);

if (isset($s[$o2])) {
    var_dump($s[$o2]);
}
?>
```

Результат виконання наведеного прикладу:

```
array(3) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
}
```

## Зміст

-   [SplObjectStorage::addAll](splobjectstorage.addall.md)— Додає всі об'єкти з іншого контейнера
-   [SplObjectStorage::attach](splobjectstorage.attach.md)— Додає об'єкт у контейнер
-   [SplObjectStorage::contains](splobjectstorage.contains.md)— Перевіряє, чи контейнер містить заданий об'єкт
-   [SplObjectStorage::count](splobjectstorage.count.md)— Повертає кількість об'єктів у контейнері
-   [SplObjectStorage::current](splobjectstorage.current.md)— Повертає поточний об'єкт
-   [SplObjectStorage::detach](splobjectstorage.detach.md)— Видаляє об'єкт з контейнера
-   [SplObjectStorage::getHash](splobjectstorage.gethash.md) \- Обчислює унікальний ідентифікатор для об'єктів контейнера
-   [SplObjectStorage::getInfo](splobjectstorage.getinfo.md)— Повертає дані, що асоціюються з поточним об'єктом
-   [SplObjectStorage::key](splobjectstorage.key.md) \- Повертає індекс поточного положення ітератора
-   [SplObjectStorage::next](splobjectstorage.next.md)— Перехід до наступного об'єкту
-   [SplObjectStorage::offsetExists](splobjectstorage.offsetexists.md)— Перевіряє, чи існує об'єкт у контейнері
-   [SplObjectStorage::offsetGet](splobjectstorage.offsetget.md)— Повертає дані, що асоціюються з об'єктом object
-   [SplObjectStorage::offsetSet](splobjectstorage.offsetset.md)— Асоціює дані з об'єктом у контейнері
-   [SplObjectStorage::offsetUnset](splobjectstorage.offsetunset.md)— Видаляє об'єкт із контейнера
-   [SplObjectStorage::removeAll](splobjectstorage.removeall.md)— Видаляє з поточного контейнера об'єкти, які є в іншому контейнері
-   [SplObjectStorage::removeAllExcept](splobjectstorage.removeallexcept.md)— Видаляє з поточного контейнера всі об'єкти, яких немає в іншому контейнері
-   [SplObjectStorage::rewind](splobjectstorage.rewind.md) \- Переводить ітератор на перший елемент контейнера
-   [SplObjectStorage::serialize](splobjectstorage.serialize.md) \- Серіалізує контейнер
-   [SplObjectStorage::setInfo](splobjectstorage.setinfo.md)— Асоціює дані з поточним об'єктом контейнера
-   [SplObjectStorage::unserialize](splobjectstorage.unserialize.md)— Відновлює серіалізований контейнер із рядка
-   [SplObjectStorage::valid](splobjectstorage.valid.md)— Визначає, чи допустиме поточне значення ітератора
