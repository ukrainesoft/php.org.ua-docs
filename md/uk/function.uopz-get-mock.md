Отримати поточний імітатор для класу

-   [« uopzgethook](function.uopz-get-hook.html)
    
-   [uopzgetproperty »](function.uopz-get-property.html)
    
-   [PHP Manual](index.html)
    
-   [Функції Uopz](ref.uopz.html)
    
-   Отримати поточний імітатор для класу
    

# uopzgetmock

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopzgetmock — Отримати поточний імітатор для класу.

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

**Приклад #1 Приклад використання **uopzgetmock()****

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
echo uopz_get_mock(A::class);
?>
```

Результат виконання цього прикладу:

```
mockA
```

### Дивіться також

-   [uopzsetmock()](function.uopz-set-mock.html) - Використовувати імітатор замість класу для нових об'єктів
-   [uopzunsetmock()](function.uopz-unset-mock.html) - Видалити раніше встановлений імітатор