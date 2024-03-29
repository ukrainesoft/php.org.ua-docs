---
navigation:
  - function.uopz-extend.md: « uopz\_extend
  - function.uopz-function.md: uopz\_function »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_flags
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_flags

(PECL uopz 2 >= 2.0.2, PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopz\_flags — Отримати або встановити прапори для функції або класу

### Опис

```methodsynopsis
uopz_flags(string $function, int $flags = PHP_INT_MAX): int
```

```methodsynopsis
uopz_flags(string $class, string $function, int $flags = PHP_INT_MAX): int
```

Отримати або встановити прапори для запису функції або класу під час виконання

### Список параметрів

`class`

Ім'я класу

`function`

Ім'я функції. Якщо заданий `class`и пустая строка передана как`function` **uopz\_flags()** отримує чи встановлює прапори запису класу.

`flags`

Коректний набір прапорів ZEND\_ACC\_. Якщо не задано, **uopz\_flags()** використовується як гетер.

### Значення, що повертаються

При встановленні нових прапорів повертає старі прапори, інакше повертає поточні прапори.

### Помилки

Починаючи з PHP 7.4.0, якщо передано параметр `flags` **uopz\_extends()** викидає [RuntimeException](class.runtimeexception.md), якщо [OPcache](book.opcache.md) включений і запис класу або `class`, либо`parent` (якщо це ознака) незмінні.

### список змін

| Версия | Опис |
| --- | --- |
| PECL uopz 5.0.0 | Параметр`flags` тепер необов'язковий. Раніше **`ZEND_ACC_FETCH`** мав передаватися, щоб **uopz\_flags()** використовувався як геттер. |

### Приклади

**Приклад #1 Приклад використання** uopz\_flags()\*\*\*\*

```php
<?php
class Test {
    public function method() {
        return __CLASS__;
    }
}

$flags = uopz_flags("Test", "method");

var_dump((bool) (uopz_flags("Test", "method") & ZEND_ACC_PRIVATE));
var_dump((bool) (uopz_flags("Test", "method") & ZEND_ACC_STATIC));

var_dump(uopz_flags("Test", "method", $flags|ZEND_ACC_STATIC|ZEND_ACC_PRIVATE));

var_dump((bool) (uopz_flags("Test", "method") & ZEND_ACC_PRIVATE));
var_dump((bool) (uopz_flags("Test", "method") & ZEND_ACC_STATIC));
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(false)
int(1234567890)
bool(true)
bool(true)
```

**Приклад #2 "Скасувати final" класу**

```php
<?php
final class MyClass
{
}

$flags = uopz_flags(MyClass::class, '');
uopz_flags(MyClass::class, '', $flags & ~ZEND_ACC_FINAL);
var_dump((new ReflectionClass(MyClass::class))->isFinal());
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
```
