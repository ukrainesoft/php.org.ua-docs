---
navigation:
  - closure.fromcallable.md: '« Closure::fromCallable'
  - class.generator.md: Generator »
  - index.md: PHP Manual
  - reserved.interfaces.md: Вбудовані інтерфейси та класи
title: Клас stdClass
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас stdClass

(PHP 4, PHP 5, PHP 7, PHP 8)

## Вступ

Порожній клас загального призначення із динамічними властивостями.

Об'єкти класу можуть бути ініціалізовані за допомогою оператора [new](language.oop5.basic.md#language.oop5.basic.new) або створені за допомогою [перетворення на об'єкт](language.types.object.md#language.types.object.casting). Деякі функції PHP також створюють екземпляри цього класу, наприклад функції [json\_decode()](function.json-decode.md) [mysqli\_fetch\_object()](mysqli-result.fetch-object.md) або [PDOStatement::fetchObject()](pdostatement.fetchobject.md)

Незважаючи на відсутність реалізації магічних методів [\_\_get()](language.oop5.overloading.md#object.get) [\_\_set()](language.oop5.overloading.md#object.set), клас дозволяє використовувати динамічні властивості та не вимагає атрибуту `#[\AllowDynamicProperties]`

Це не базовий клас, оскільки PHP немає поняття універсального базового класу. Однак можна створити власний клас, який розширює **stdClass** і в результаті успадковує функціональність динамічних властивостей.

## Огляд класів

```classsynopsis

    
     class stdClass
     {
   }
```

Клас не має методів або властивостей за замовчуванням.

## Приклади

**Приклад #1 Створення в результаті перетворення на об'єкт**

```php
<?php
$obj = (object) array('foo' => 'bar');
var_dump($obj);
```

Результат виконання наведеного прикладу:

```
object(stdClass)#1 (1) {
  ["foo"]=>
  string(3) "bar"
}
```

**Приклад #2 Створення внаслідок роботи функції [json\_decode()](function.json-decode.md)**

```php
<?php
$json = '{"foo":"bar"}';
var_dump(json_decode($json));
```

Результат виконання наведеного прикладу:

```
object(stdClass)#1 (1) {
  ["foo"]=>
  string(3) "bar"
}
```

**Приклад #3 Оголошення динамічних властивостей**

```php
<?php
$obj = new stdClass();
$obj->foo = 42;
$obj->{1} = 42;
var_dump($obj);
```

Результат виконання наведеного прикладу:

```
object(stdClass)#1 (2) {
  ["foo"]=>
  int(42)
  ["1"]=>
  int(42)
}
```
