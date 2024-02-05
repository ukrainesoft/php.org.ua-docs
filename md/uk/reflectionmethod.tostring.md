---
navigation:
  - reflectionmethod.setaccessible.md: '« ReflectionMethod::setAccessible'
  - class.reflectionnamedtype.md: ReflectionNamedType »
  - index.md: PHP Manual
  - class.reflectionmethod.md: ReflectionMethod
title: 'ReflectionMethod::\_\_function toString() { \[native code\] }'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionMethod::\_\_function toString() { \[native code\] }

(PHP 5, PHP 7, PHP 8)

ReflectionMethod::\_\_toString — Повертає строкове представлення об'єкта ReflectionMethod

### Опис

```methodsynopsis
public ReflectionMethod::__toString(): string
```

Повертає рядкову виставу об'єкта ReflectionMethod.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Строкове представлення об'єкта [ReflectionMethod](class.reflectionmethod.md)

### Приклади

**Пример #1 Пример использования**ReflectionMethod::\_\_toString()\*\*\*\*

```php
<?php
class HelloWorld {

    public function sayHelloTo($name) {
        return 'Привет, ' . $name;
    }

}

$reflectionMethod = new ReflectionMethod(new HelloWorld(), 'sayHelloTo');
echo $reflectionMethod;
?>
```

Результат виконання наведеного прикладу:

```
Method [ <user> public method sayHelloTo ] {
  @@ /var/www/examples/reflection.php 16 - 18

  - Parameters [1] {
    Parameter #0 [ <required> $name ]
  }
}
```

### Дивіться також

-   [ReflectionMethod::export()](reflectionmethod.export.md) \- Експорт відбитого методу
-   [\_\_toString()](language.oop5.magic.md#object.tostring)
