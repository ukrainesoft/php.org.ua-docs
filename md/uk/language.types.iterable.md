Ітеровані

-   [« Массивы](language.types.array.html)
    
-   [Объекты »](language.types.object.html)
    
-   [PHP Manual](index.html)
    
-   [Типы](language.types.html)
    
-   Ітеровані
    

## Ітеровані

[Iterable](language.types.iterable.html) - псевдотип, введений у PHP 7.1. Він приймає будь-який масив (array) або об'єкт, що реалізує інтерфейс [Traversable](class.traversable.html). Обидва ці типи ітеруються за допомогою [foreach](control-structures.foreach.html) і можуть бути використані з **yield from** в [генераторах](language.generators.html)

### Використання Iterable

Тип iterable може використовуватися як тип параметра для вказівки, що функція набирає значень, але їй не важлива форма цього набору, поки він буде використовуватися з [foreach](control-structures.foreach.html). Якщо значення не є масивом або об'єктом, що реалізує [Traversable](class.traversable.html), буде викинуто виняток [TypeError](class.typeerror.html)

**Приклад #1 Приклад використання iterable як параметр**

```php
<?php

function foo(iterable $iterable) {
    foreach ($iterable as $value) {
        // ...
    }
}

?>
```

Параметри, оголошені як iterable, можуть використовувати **`null`** або масив як значення за замовчуванням.

**Приклад #2 Приклад установки за промовчанням для iterable**

```php
<?php

function foo(iterable $iterable = []) {
    // ...
}

?>
```

Iterable також може використовуватися як тип, що повертається для вказівки, що функція поверне значення, що ітерується. Якщо значення, що повертається, не є масивом або об'єктом, що реалізує [Traversable](class.traversable.html), буде викинуто виняток [TypeError](class.typeerror.html)

**Приклад #3 Приклад використання iterable як тип, що повертається**

```php
<?php

function bar(): iterable {
    return [1, 2, 3];
}

?>
```

Функції, що оголошують iterable як тип, що повертається, також можуть бути [генераторами](language.generators.html)

**Приклад #4 Приклад використання iterable як значення генератора, що повертається**

```php
<?php

function gen(): iterable {
    yield 1;
    yield 2;
    yield 3;
}

?>
```