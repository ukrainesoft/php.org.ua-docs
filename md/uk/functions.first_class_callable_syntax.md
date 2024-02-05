---
navigation:
  - functions.arrow.md: « Стрілкові функції
  - language.oop5.md: Класи та об'єкти »
  - index.md: PHP Manual
  - language.functions.md: Функції
title: Callback-функції як об'єкти першого класу
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Callback-функції як об'єкти першого класу

Callback-функції як об'єкти першого класу представлені в PHP 8.1.0 як спосіб створення [анонімних функцій](functions.anonymous.md)из[callback-функцій](language.types.callable.md). Синтаксис замінює існуючий синтаксис виклику з використанням рядків та масивів. Перевага синтаксису полягає в тому, що він доступний для статичного аналізу та використовує область видимості у точці, де отримана callback-функція.

Синтаксис`CallableExpr(...)` використовується для створення об'єкта [Closure](class.closure.md)из callback-функции`CallableExpr` приймає будь-який вираз, який може бути викликаний безпосередньо в граматиці PHP:

**Приклад #1 Простий приклад callback функції як об'єкти першого класу**

```php
<?php
class Foo {
   public function method() {}
   public static function staticmethod() {}
   public function __invoke() {}
}
$obj = new Foo();
$classStr = 'Foo';
$methodStr = 'method';
$staticmethodStr = 'staticmethod';
$f1 = strlen(...);
$f2 = $obj(...);  // вызываемый объект
$f3 = $obj->method(...);
$f4 = $obj->$methodStr(...);
$f5 = Foo::staticmethod(...);
$f6 = $classStr::$staticmethodStr(...);
// традиционная callback-функция с использованием строки, массива
$f7 = 'strlen'(...);
$f8 = [$obj, 'method'](...);
$f9 = [Foo::class, 'staticmethod'](...);
?>
```

> **Зауваження** :
> 
> `...`является частью синтаксиса, а не пропуском.

У`CallableExpr(...)` та ж семантика, що й у [Closure::fromCallable()](closure.fromcallable.md). Тобто, на відміну від callback-функції з використанням рядків та масивів, `CallableExpr(...)` враховує область видимості у точці, де вона створюється:

**Приклад #2 Сравнение области действия`CallableExpr(...)` та традиційної callback-функції**

```php
<?php
class Foo {
    public function getPrivateMethod() {
        return [$this, 'privateMethod'];
    }
    private function privateMethod() {
        echo __METHOD__, "\n";
    }
}
$foo = new Foo;
$privateMethod = $foo->getPrivateMethod();
$privateMethod();
// Fatal error: Call to private method Foo::privateMethod() from global scope
// Это потому, что вызов выполняется вне Foo, и с этого момента будет проверяться видимость.
class Foo1 {
    public function getPrivateMethod() {
        // Использует область, в которой получена callback-функция.
        return $this->privateMethod(...); // идентично Closure::fromCallable([$this, 'privateMethod']);
    }
    private function privateMethod() {
        echo __METHOD__, "\n";
    }
}
$foo1 = new Foo1;
$privateMethod = $foo1->getPrivateMethod();
$privateMethod();  // Foo1::privateMethod
?>
```

> **Зауваження** :
> 
> Створення об'єкта за допомогою цього синтаксису (наприклад, `new Foo(...)`) не підтримується, оскільки синтаксис `new Foo()` не вважається callback-функцією.

> **Зауваження** :
> 
> Callback-функції як об'єкти першого класу не можна комбінувати з [оператором Nullsafe](language.oop5.basic.md#language.oop5.basic.nullsafe)Оба следующих результата приводят к ошибке времени компиляции:
> 
> ```php
> <?php
> $obj?->method(...);
> $obj?->prop->method(...);
> ?>
> ```
