---
navigation:
  - function.uopz-get-hook.md: « uopz\_get\_hook
  - function.uopz-get-property.md: uopz\_get\_property »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_get\_mock
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_get\_mock

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopz\_get\_mock — Отримати поточний імітатор для класу.

### Опис

```methodsynopsis
uopz_get_mock(string $class): mixed
```

Повертає поточний імітатор `class`

### Список параметрів

`class`

Назва імітованого класу

### Значення, що повертаються

Або рядок, що містить назву імітатора, або об'єкт, або \*\*`null`\*\*якщо імітатор не заданий.

### Приклади

**Приклад #1 Приклад використання** uopz\_get\_mock()\*\*\*\*

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
echo uopz_get_mock(A::class);
?>
```

Результат виконання наведеного прикладу:

```
mockA
```

### Дивіться також

-   [uopz\_set\_mock()](function.uopz-set-mock.md) \- Використовувати імітатор замість класу для нових об'єктів
-   [uopz\_unset\_mock()](function.uopz-unset-mock.md) \- Видалити раніше встановлений імітатор
