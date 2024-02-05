---
navigation:
  - function.uopz-set-mock.md: « uopz\_set\_mock
  - function.uopz-set-return.md: uopz\_set\_return »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_set\_property
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_set\_property

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopz\_set\_property — Встановлює значення існуючої властивості класу або екземпляра

### Опис

```methodsynopsis
uopz_set_property(string $class, string $property, mixed $value): void
```

```methodsynopsis
uopz_set_property(object $instance, string $property, mixed $value): void
```

Задає значення статичної властивості класу, якщо заданий клас (`class`), або значення існуючої властивості екземпляра (незалежно від того, чи існує властивість екземпляра), якщо передано екземпляр (`instance`

### Список параметрів

`class`

Назва класу.

`instance`

Примірник об'єкта.

`property`

Ім'я якості.

`value`

Значення, що присвоюється властивістю.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Простое использование**uopz\_set\_property()\*\*\*\*

```php
<?php
class Foo {
   private static $staticBar;
   private $bar;
   public static function testStaticBar() {
      return self::$staticBar;
   }
   public function testBar() {
      return $this->bar;
   }
}
$foo = new Foo;
uopz_set_property('Foo', 'staticBar', 10);
uopz_set_property($foo, 'bar', 100);
var_dump(Foo::testStaticBar());
var_dump($foo->testBar());
?>
```

Результат виконання наведеного прикладу:

```
int(10)
```

### Дивіться також

-   [uopz\_get\_property()](function.uopz-get-property.md) \- Отримує значення класу або властивість екземпляра
