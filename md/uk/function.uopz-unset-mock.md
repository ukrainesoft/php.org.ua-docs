Видалити раніше встановлений імітатор

-   [« uopz\_unset\_hook](function.uopz-unset-hook.html)
    
-   [uopz\_unset\_return »](function.uopz-unset-return.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Uopz](ref.uopz.html)
    
-   Видалити раніше встановлений імітатор
    

# uopzunsetmock

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopzunsetmock — Видалити раніше встановлений імітатор

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

Викидає [RuntimeException](class.runtimeexception.html), якщо раніше не було встановлено імітатор для `class`

### Приклади

**Приклад #1 Приклад використання **uopzunsetmock()****

```php
<?php
class A {
    public static function who() {
        echo "A";
    }
}

class mockA {
    public static function who() {
        echo "mockA";
    }
}

uopz_set_mock(A::class, mockA::class);
uopz_unset_mock(A::class);
A::who();
?>
```

Результат виконання цього прикладу:

```
A
```

### Дивіться також

-   [uopz\_set\_mock()](function.uopz-set-mock.html) - Використовувати імітатор замість класу для нових об'єктів
-   [uopz\_get\_mock()](function.uopz-get-mock.html) - отримати поточний імітатор (mock) для класу