---
navigation:
  - function.class-exists.html: « classexists
  - function.get-called-class.html: getcalledclass »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: enumexists
---
# enumexists

(PHP 8> = 8.1.0)

enumexists — Перевіряє, чи визначено перерахування

### Опис

```methodsynopsis
enum_exists(string $enum, bool $autoload = true): bool
```

Функція перевіряє, чи визначено цей перелік.

### Список параметрів

`enum`

Ім'я переліку. Ім'я зіставляється без урахування регістру.

`autoload`

Чи слід викликати [autoload](language.oop5.autoload.md) за замовчуванням.

### Значення, що повертаються

Повертає **`true`**, якщо перерахування `enum` визначено або **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **enumexists()****

```php
<?php
// Убедитесь, что перечисление существует, прежде чем пытаться его использовать
if (enum_exists(Suit::class)) {
    $myclass = Suit::Hearts;
}
?>
```

### Дивіться також

-   [functionexists()](function.function-exists.md) - Повертає true, якщо вказана функція визначена
-   [classexists()](function.class-exists.md) - Перевіряє, чи був оголошений клас
-   [interfaceexists()](function.interface-exists.md) - Перевіряє, чи визначено інтерфейс
-   [getdeclaredclasses()](function.get-declared-classes.md) - Повертає масив із іменами оголошених класів
