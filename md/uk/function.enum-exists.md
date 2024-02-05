---
navigation:
  - function.class-exists.md: « class\_exists
  - function.get-called-class.md: get\_called\_class »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: enum\_exists
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# enum\_exists

(PHP 8 >= 8.1.0)

enum\_exists — Перевіряє, чи визначено перерахування

### Опис

```methodsynopsis
enum_exists(string $enum, bool $autoload = true): bool
```

Функция проверяет, определено ли данное[перерахування](language.enumerations.md)

### Список параметрів

`enum`

Ім'я переліку. Ім'я зіставляється без урахування регістру.

`autoload`

Чи потрібно [автоматично підвантажувати](language.oop5.autoload.md) клас, якщо він ще не завантажений.

### Значення, що повертаються

Повертає **`true`**, якщо перерахування `enum`определено или\*\*`false`\*\* в іншому випадку.

### Приклади

**Пример #1 Пример использования**enum\_exists()\*\*\*\*

```php
<?php
// Убедитесь, что перечисление существует, прежде чем пытаться его использовать
if (enum_exists(Suit::class)) {
    $myclass = Suit::Hearts;
}
?>
```

### Дивіться також

-   [function\_exists()](function.function-exists.md) \- Повертає true, якщо вказана функція визначена
-   [class\_exists()](function.class-exists.md) \- Перевіряє, чи був оголошений клас
-   [interface\_exists()](function.interface-exists.md) \- Перевіряє, чи визначено інтерфейс
-   [get\_declared\_classes()](function.get-declared-classes.md) \- Повертає масив із іменами оголошених класів
