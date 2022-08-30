Інтерфейс Hashable

-   [« DsCollection::toArray](ds-collection.toarray.html)
    
-   [ДсHashable::equals »](ds-hashable.equals.html)
    
-   [PHP Manual](index.md)
    
-   [Структури даних](book.ds.md)
    
-   Інтерфейс Hashable
    

# Інтерфейс Hashable

(No version information available, might only be in Git)

## Вступ

Hashable - це інтерфейс, який дозволяє використовувати об'єкти як ключі. Це альтернатива функції [splobjecthash()](function.spl-object-hash.html), яка обчислює хеш об'єкта відповідно до його обробником: це означає, що два об'єкти можуть бути однакові за своїм станом, але не вважаються однаковими через те, що є різними екземплярами одного класу.

Функція [hash()](function.hash.md) використовується для обчислення скалярного значення, що характеризує хеш об'єкта та визначає його положення в хеш-таблиці. Хоча це значення необов'язково має бути унікальним, однакові об'єкти повинні мати те саме значення хеша.

Функція **equals()** використовується визначення ідентичності двох об'єктів. Вона гарантує, що два об'єкти є одним і тим самим екземпляром класу.

## Огляд інтерфейсів

```classsynopsis


    
    
     
      class Ds\Hashable
     
     {
    

    /* Методы */
    
   abstract public equals(object $obj): bool
abstract public hash(): mixed

   }
```

## Зміст

-   [ДсHashable::equals](ds-hashable.equals.html) — Визначає, чи дорівнює поточний екземпляр переданому об'єкту
-   [ДсHashable::hash](ds-hashable.hash.html) — Повертає скалярне значення для використання як значення хешу