---
navigation:
  - language.oop5.magic.md: Магічні методи
  - language.oop5.cloning.md: Клонування об'єктів »
  - index.md: PHP Manual
  - language.oop5.md: Класи та об'єкти
title: Ключове слово final
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Ключове слово final

PHP предоставляет ключевое слово`final`, Розмістивши яке перед оголошеннями методів або констант класу, можна запобігти їх перевизначення в дочірніх класах. Якщо ж клас визначається з цим ключовим словом, він зможе бути успадкований.

**Приклад #1 Приклад остаточних методів**

```php
<?php
class BaseClass {
   public function test() {
       echo "Вызван метод BaseClass::test()\n";
   }

   final public function moreTesting() {
       echo "Вызван метод BaseClass::moreTesting()\n";
   }
}

class ChildClass extends BaseClass {
   public function moreTesting() {
       echo "Вызван метод ChildClass::moreTesting()\n";
   }
}
// Выполнение заканчивается фатальной ошибкой: Cannot override final method BaseClass::moreTesting()
// (Окончательный (final) метод BaseClass::moreТesting() не может быть переопределён)
?>
```

**Приклад #2 Приклад остаточного (final) класу**

```php
<?php
final class BaseClass {
   public function test() {
       echo "Вызван метод BaseClass::test()\n";
   }

   // Поскольку класс уже является final, ключевое слово final является избыточным
   final public function moreTesting() {
       echo "BaseClass::moreTesting() called\n";
   }
}

class ChildClass extends BaseClass {
}
// Выполнение заканчивается фатальной ошибкой: Class ChildClass may not inherit from final class (BaseClass)
// (Класс ChildClass не может быть унаследован от окончательного класса (BaseClass))
?>
```

**Приклад #3 Приклад остаточної константи класу, починаючи з PHP 8.1.0**

```php
<?php
class Foo
{
    final public const X = "foo";
}

class Bar extends Foo
{
    public const X = "bar";
}

// Ошибка: Bar::X не может переопределить окончательную константу Foo::X
?>
```

> **Зауваження**: Властивості не можуть бути оголошені остаточними: тільки класи, методи та константи (починаючи з PHP 8.1.0) можуть бути оголошені як остаточні (final). Починаючи з PHP 8.0.0, закриті методи не можуть бути оголошені остаточними, за винятком конструктора.
