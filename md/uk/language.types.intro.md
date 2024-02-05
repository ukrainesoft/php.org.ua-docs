---
navigation:
  - language.types.md: « Типи
  - language.types.type-system.md: Система типів »
  - index.md: PHP Manual
  - language.types.md: Типи
title: Вступ
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Вступ

У кожного виразу в PHP один із наступних вбудованих типів залежно від його значення:

-   null
-   bool
-   int
-   float (floating-point number)
-   string
-   array
-   object
-   [callable](language.types.callable.md)
-   resource

PHP – динамічно типізована мова, що означає, що за замовчуванням немає необхідності вказувати тип змінної, оскільки вона буде визначена під час виконання. Проте можна статично типізувати деякі аспекти мови, використовуючи [декларації типів](language.types.declarations.md)

Типи обмежують тип операцій, які можуть бути виконані з них. Однак, якщо вираз/змінна використовується в операції, яку не підтримує її тип, PHP спробує [перетворити](language.types.type-juggling.md) значення тип, який підтримує операцію. Цей процес залежить від контексту, де використовується значення. Для отримання додаткової інформації дивіться розділ [Маніпуляції з типами](language.types.type-juggling.md)

**Підказка**

[Таблиці порівняння типів](types.comparisons.md) також можуть бути корисними, оскільки в них представлені різні приклади порівняння значень різних типів.

> **Зауваження**: Можна змусити вираз оцінюватися з певним типом, використовуючи [приведення типів](language.types.type-juggling.md#language.types.typecasting). Змінна також може бути наведена до певного типу за допомогою функції [settype()](function.settype.md)

Щоб перевірити значення та тип [вирази](language.expressions.md), используйте функцию[var\_dump()](function.var-dump.md). Щоб отримати тип [вирази](language.expressions.md), используйте функцию[get\_debug\_type()](function.get-debug-type.md). Проте, щоб перевірити, чи є вираз певним типом, використовуйте функції `is_type`

```php
<?php
$a_bool = true;   // логическое значение
$a_str  = "foo";  // строка
$a_str2 = 'foo';  // строка
$an_int = 12;     // целое число

echo get_debug_type($a_bool), "\n";
echo get_debug_type($a_str), "\n";

// Если это целое число, увеличить на четыре
if (is_int($an_int)) {
    $an_int += 4;
}
var_dump($an_int);

// Если $a_bool - это строка, вывести её
if (is_string($a_bool)) {
    echo "Строка: $a_bool";
}
?>
```

Результат виконання наведеного прикладу в PHP 8:

```
bool
string
int(16)
```

> **Зауваження**: Замість функції [get\_debug\_type()](function.get-debug-type.md), яка була недоступна до PHP 8.0.0, викликали функцію [gettype()](function.gettype.md). Проте вона повертає канонічні імена типів.
