---
navigation:
  - function.uopz-unset-hook.md: « uopz\_unset\_hook
  - function.uopz-unset-return.md: uopz\_unset\_return »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_unset\_mock
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_unset\_mock

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopz\_unset\_mock — Видалити раніше встановлений імітатор

### Опис

```methodsynopsis
uopz_unset_mock(string $class): void
```

Видаляє раніше встановлений імітатор для `class`

### Список параметрів

`class`

Ім'я класу, що імітує.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає [RuntimeException](class.runtimeexception.md), якщо раніше не було встановлено імітатор для `class`

### Приклади

**Приклад #1 Приклад використання** uopz\_unset\_mock()\*\*\*\*

```php
<?php
class A {
    public static function who() {
        echo "A";
    }
}

class mockA {
    public static function who() {
        echo "mockA";
    }
}

uopz_set_mock(A::class, mockA::class);
uopz_unset_mock(A::class);
A::who();
?>
```

Результат виконання наведеного прикладу:

```
A
```

### Дивіться також

-   [uopz\_set\_mock()](function.uopz-set-mock.md) \- Використовувати імітатор замість класу для нових об'єктів
-   [uopz\_get\_mock()](function.uopz-get-mock.md) \- отримати поточний імітатор (mock) для класу
