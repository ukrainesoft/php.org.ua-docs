---
navigation:
  - function.floatval.md: « floatval
  - function.get-defined-vars.md: getdefinedvars »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: getdebugtype
---
# getdebugtype

(PHP 8)

getdebugtype — Повертає назву типу змінної у вигляді, що підходить для налагодження

### Опис

```methodsynopsis
get_debug_type(mixed $value): string
```

Повертає перетворене ім'я змінної PHP `value`. Функція перетворює об'єкти в ім'я їхнього класу, ресурси - в ім'я їхнього типу ресурсу, а скалярні значення - у загальноприйняте ім'я їхнього типу, яке б використовувалося в оголошенні типів.

Функція відрізняється від [gettype()](function.gettype.md) тим, що повертає імена типів, які більше відповідають фактичному використанню, а не ті, що є з історичних причин.

### Список параметрів

`value`

Змінна, яка перевіряє тип.

### Значення, що повертаються

Можливі значення для рядка, що повертається:

| Тип + Состояние | Возвращаемое значение | Замечания |
| --- | --- | --- |
| null | `"null"` |  |
| Логічні значення (true чи false) | `"bool"` |  |
| Цілі числа | `"int"` |  |
| Числа з плаваючою точкою | `"float"` |  |
| Рядки | `"string"` |  |
| Масиви | `"array"` |  |
| Ресурси | `"resource (resourcename)"` |  |
| Ресурси (закриті) | `"resource (closed)"` | Приклад: файловий потік після закриття з допомогою fclose. |
| Об'єкти іменованих класів | Повне ім'я класу, включаючи його простір імен, наприклад, `Foo\Bar` |  |
| Об'єкти анонімних класів | `"class@anonymous"` | Анонімні класи - це класи, створені за допомогою синтаксису $x = new class { ... }. |

### Приклади

**Приклад #1 Приклад використання **getdebugtype()****

```php
<?php
echo get_debug_type(null) . PHP_EOL;
echo get_debug_type(true) . PHP_EOL;
echo get_debug_type(1) . PHP_EOL;
echo get_debug_type(0.1) . PHP_EOL;
echo get_debug_type("foo") . PHP_EOL;
echo get_debug_type([]) . PHP_EOL;

$fp = fopen(__FILE__, 'rb');
echo get_debug_type($fp) . PHP_EOL;

fclose($fp);
echo get_debug_type($fp) . PHP_EOL;

echo get_debug_type(new stdClass) . PHP_EOL;
echo get_debug_type(new class {}) . PHP_EOL;
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
null
bool
int
float
string
array
resource (stream)
resource (closed)
stdClass
class@anonymous
```

### Дивіться також

-   [gettype()](function.gettype.md) - Повертає тип змінної
-   [getclass()](function.get-class.md) - Повертає ім'я класу, до якого належить об'єкт
