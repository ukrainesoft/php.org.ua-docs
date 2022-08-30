Клас SplObjectStorage

-   [« SplFixedArray::wakeup](splfixedarray.wakeup.html)
    
-   [SplObjectStorage::addAll »](splobjectstorage.addall.html)
    
-   [PHP Manual](index.html)
    
-   [Структури даних](spl.datastructures.html)
    
-   Клас SplObjectStorage
    

# Клас SplObjectStorage

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Клас SplObjectStorage надає відображення об'єктів даних або набір об'єктів, ігноруючи дані. Ця подвійна мета може бути корисною у багатьох випадках, включаючи необхідність унікальної ідентифікації об'єктів.

## Огляд класів

```classsynopsis

     
    

    
     
      class SplObjectStorage
     

     implements 
       Countable,  Iterator,  Serializable,  ArrayAccess {

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

**Приклад #1 Клас **SplObjectStorage** як набір об'єктів**

```php
<?php
// Набор объектов
$s = new SplObjectStorage();

$o1 = new StdClass;
$o2 = new StdClass;
$o3 = new StdClass;

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

Результат виконання цього прикладу:

```
bool(true)
bool(true)
bool(false)
bool(true)
bool(false)
bool(false)
```

**Приклад #2 Клас **SplObjectStorage** як відображення об'єктів у дані**

```php
<?php
// Как отображение объектов к данным
$s = new SplObjectStorage();

$o1 = new StdClass;
$o2 = new StdClass;
$o3 = new StdClass;

$s[$o1] = "данные для объекта 1";
$s[$o2] = array(1,2,3);

if (isset($s[$o2])) {
    var_dump($s[$o2]);
}
?>
```

Результат виконання цього прикладу:

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

-   [SplObjectStorage::addAll](splobjectstorage.addall.html) — Додає всі об'єкти з іншого контейнера
-   [SplObjectStorage::attach](splobjectstorage.attach.html) — Додає об'єкт у контейнер
-   [SplObjectStorage::contains](splobjectstorage.contains.html) — Перевіряє, чи контейнер містить заданий об'єкт
-   [SplObjectStorage::count](splobjectstorage.count.html) — Повертає кількість об'єктів у контейнері
-   [SplObjectStorage::current](splobjectstorage.current.html) — Повертає поточний об'єкт
-   [SplObjectStorage::detach](splobjectstorage.detach.html) — Видаляє об'єкт з контейнера
-   [SplObjectStorage::getHash](splobjectstorage.gethash.html) - Обчислює унікальний ідентифікатор для об'єктів контейнера
-   [SplObjectStorage::getInfo](splobjectstorage.getinfo.html) — Повертає дані, що асоціюються з поточним об'єктом
-   [SplObjectStorage::key](splobjectstorage.key.html) - Повертає індекс поточного положення ітератора
-   [SplObjectStorage::next](splobjectstorage.next.html) — Перехід до наступного об'єкту
-   [SplObjectStorage::offsetExists](splobjectstorage.offsetexists.html) — Перевіряє, чи існує об'єкт у контейнері
-   [SplObjectStorage::offsetGet](splobjectstorage.offsetget.html) — Повертає дані, що асоціюються з об'єктом object
-   [SplObjectStorage::offsetSet](splobjectstorage.offsetset.html) — Асоціює дані з об'єктом у контейнері
-   [SplObjectStorage::offsetUnset](splobjectstorage.offsetunset.html) — Видаляє об'єкт із контейнера
-   [SplObjectStorage::removeAll](splobjectstorage.removeall.html) — Видаляє з поточного контейнера об'єкти, які є в іншому контейнері
-   [SplObjectStorage::removeAllExcept](splobjectstorage.removeallexcept.html) — Видаляє з поточного контейнера всі об'єкти, яких немає в іншому контейнері
-   [SplObjectStorage::rewind](splobjectstorage.rewind.html) - Переводить ітератор на перший елемент контейнера
-   [SplObjectStorage::serialize](splobjectstorage.serialize.html) - Серіалізує контейнер
-   [SplObjectStorage::setInfo](splobjectstorage.setinfo.html) — Асоціює дані з поточним об'єктом контейнера
-   [SplObjectStorage::unserialize](splobjectstorage.unserialize.html) — Відновлює серіалізований контейнер із рядка
-   [SplObjectStorage::valid](splobjectstorage.valid.html) — Визначає, чи допустиме поточне значення ітератора