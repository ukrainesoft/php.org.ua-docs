- [« ReflectionClass::getParentClass](reflectionclass.getparentclass.md)
- [ReflectionClass::getProperty »](reflectionclass.getproperty.md)

- [PHP Manual](index.md)
- [ReflectionClass](class.reflectionclass.md)
- Повертає властивості

# ReflectionClass::getProperties

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getProperties — Повертає властивості

### Опис

public **ReflectionClass::getProperties**(?int `$filter` = **`null`**):
array

Повертає reflected (відбиті) властивості.

### Список параметрів

`filter`
Опціональний фільтр, що дозволяє повертати лише бажані типи
властивостей. Він налаштовується за допомогою [констант ReflectionProperty](class.reflectionproperty.md#reflectionproperty.constants.modifiers),
за замовчуванням дає змогу повертати властивості всіх типів.

### Значення, що повертаються

Масив об'єктів класу
[ReflectionProperty](class.reflectionproperty.md).

### Список змін

| Версія | Опис                                  |
| ------ | ------------------------------------- |
| 7.2.0  | filter тепер припускає значення null. |

### Приклади

**Приклад #1 Приклад фільтрації за допомогою
**ReflectionClass::getProperties()****

У цьому прикладі демонструється використання параметра `filter`, який
у разі не пропускає private (закриті) властивості.

` <?phpclass Foo {    public    $foo  = 1; protected $ $ bar = = 2; private   $baz  = 3;}$foo = new Foo();$reflect = new ReflectionClass($foo);$props  = $reflect->getProperties(ReflectionProperty::IS_PU:| $prop) {    print $prop->getName() . "
";}var_dump($props);?> `

Результатом виконання цього прикладу буде щось подібне:

foo
bar
array(2) {
[0]=>
object(ReflectionProperty)#3 (2) {
["name"]=>
string(3) "foo"
["class"]=>
string(3) "Foo"
}
[1]=>
object(ReflectionProperty)#4 (2) {
["name"]=>
string(3) "bar"
["class"]=>
string(3) "Foo"
}
}

### Дивіться також

- [ReflectionClass::getProperty()](reflectionclass.getproperty.md) -
Повертає екземпляр ReflectionProperty для якості класу
- [ReflectionProperty](class.reflectionproperty.md)
- [константи ReflectionProperty](class.reflectionproperty.md#reflectionproperty.constants.modifiers)
