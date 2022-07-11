- [« ReflectionClass::getConstructor](reflectionclass.getconstructor.md)
- [ReflectionClass::getDocComment »](reflectionclass.getdoccomment.md)

- [PHP Manual](index.md)
- [ReflectionClass](class.reflectionclass.md)
- Повертає властивості за замовчуванням

# ReflectionClass::getDefaultProperties

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getDefaultProperties — Повертає стандартні властивості.

### Опис

public **ReflectionClass::getDefaultProperties**(): array

Повертає властивості класу за замовчуванням (включаючи успадковані
властивості).

> **Примітка**:
>
> Цей метод працює тільки для статичних властивостей при використанні
> внутрішніми класами. Значення за умовчанням статичної властивості
> не можна відстежувати у класах, визначених користувачем.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Асоціативний масив властивостей за замовчуванням, ключами якого
є імена властивостей, а значеннями - відповідні значення по
замовчуванням або **`null`**, якщо цій властивості не було встановлено значення
за замовчуванням. Функція не розрізняє статичні та нестатичні властивості,
а також не надає інформацію про модифікатори видимості при
висновку.

### Приклади

**Приклад #1 Приклад використання
**ReflectionClass::getDefaultProperties()****

` <?phpclass Bar {   protected $inheritedProperty = 'успадковане властивість за мовчанням';}class Foo extends Bar {     public $property | private $privateProperty = 'закрите властивість за мовчанням'; public static $staticProperty ='статичне властивість'; public $defaultlessProperty;}$reflectionClass = new ReflectionClass('Foo');var_dump($reflectionClass->getDefaultProperties());?> `

Результат виконання цього прикладу:

array(5) {
["staticProperty"]=>
string(39) "статична властивість"
["property"]=>
string(40) "властивість за замовчуванням"
["privateProperty"]=>
string(57) "закрита властивість за замовчуванням"
["defaultlessProperty"]=>
NULL
["inheritedProperty"]=>
string(69) "успадкована властивість за умовчанням"
}

### Дивіться також

- [ReflectionClass::getProperties()](reflectionclass.getproperties.md) -
Повертає властивості
- [ReflectionClass::getStaticProperties()](reflectionclass.getstaticproperties.md) -
Повертає статичні властивості
- [ReflectionClass::getProperty()](reflectionclass.getproperty.md) -
Повертає екземпляр ReflectionProperty для якості класу
