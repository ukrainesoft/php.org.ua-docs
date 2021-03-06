- [« ReflectionClass::getReflectionConstant](reflectionclass.getreflectionconstant.md)
- [ReflectionClass::getShortName »](reflectionclass.getshortname.md)

- [PHP Manual](index.md)
- [ReflectionClass](class.reflectionclass.md)
- Отримує константи класу

# ReflectionClass::getReflectionConstants

(PHP 7 \>= 7.1.0, PHP 8)

ReflectionClass::getReflectionConstants — Отримує константи класу

### Опис

public **ReflectionClass::getReflectionConstants**(?int `$filter` =
**`null`**): array

Отримує reflected (відбиті) константи.

### Список параметрів

`filter`
Додатковий фільтр для фільтрації констант видимості. Він
налаштовується за допомогою [ReflectionClassConstant constants](class.reflectionclassconstant.md#reflectionclassconstant.constants.modifiers)
і за умовчанням використовується всім констант видимості.

### Значення, що повертаються

Масив об'єктів
[ReflectionClassConstant](class.reflectionclassconstant.md).

### Список змін

| Версія | Опис                     |
| ------ | ------------------------ |
| 8.0.0  | Доданий параметр filter. |

### Приклади

**Приклад #1 Простий приклад використання
**ReflectionClass::getReflectionConstants()****

`<?phpclass Foo {    public    const FOO = 1; protected const BAR  = 2; private   const BAZ  = 3;}$foo = new Foo();$reflect = new ReflectionClass($foo);$consts  = $reflect->getReflectionConstants();foreach  getName(). "
";}var_dump($consts);?> `

Результатом виконання цього прикладу буде щось подібне:

FOO
BAR
BAZ
array(3) {
[0]=>
object(ReflectionClassConstant)#3 (2) {
["name"]=>
string(3) "FOO"
["class"]=>
string(3) "Foo"
}
[1]=>
object(ReflectionClassConstant)#4 (2) {
["name"]=>
string(3) "BAR"
["class"]=>
string(3) "Foo"
}
[2]=>
object(ReflectionClassConstant)#5 (2) {
["name"]=>
string(3) "BAZ"
["class"]=>
string(3) "Foo"
}
}

### Дивіться також

- [ReflectionClass::getReflectionConstant()](reflectionclass.getreflectionconstant.md) -
Отримує ReflectionClassConstant для константи класу
- [ReflectionClassConstant](class.reflectionclassconstant.md)
