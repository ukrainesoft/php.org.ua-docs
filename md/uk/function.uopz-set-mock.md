Використовувати імітатор замість класу для нових об'єктів

-   [« uopz\_set\_hook](function.uopz-set-hook.html)
    
-   [uopz\_set\_property »](function.uopz-set-property.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Uopz](ref.uopz.html)
    
-   Використовувати імітатор замість класу для нових об'єктів
    

# uopzsetmock

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopzsetmock — Використовувати імітатор замість класу для нових об'єктів

### Опис

```methodsynopsis
uopz_set_mock(string $class, mixed $mock): void
```

Якщо `mock` - це рядок, що містить ім'я класу, тоді він буде створений замість `class`. . `mock` також може бути об'єктом.

> **Зауваження**
> 
> Тільки динамічний доступ до властивостей та методів буде використовувати об'єкт `mock`. Статичний доступ використовуватиме оригінальний `class`. Дивіться [пример](function.uopz-set-mock.html#uopz_set_mock.example.static) нижче.

### Список параметрів

`class`

Ім'я класу, який буде імітовано.

`mock`

Імітатор у вигляді рядка, що містить ім'я класу, що використовується, або об'єкт. Якщо передано рядок, він має містити абсолютне ім'я класу. У цьому випадку рекомендується використовувати магічну константу `::class`

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия     | Описание                                                                                                                                                                                                                                     |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| uopz 6.0.0 | Імітування статичних функцій не підтримуються цією функцією. Замість цього слід використовувати [uopz\_redefine()](function.uopz-redefine.html) і [uopz\_set\_return()](function.uopz-set-return.html), або [Componere](book.componere.html) |

### Приклади

**Приклад #1 Приклад використання **uopzsetmock()****

```php
<?php
class A {
    public function who() {
        echo "A";
    }
}

class mockA {
    public function who() {
        echo "mockA";
    }
}

uopz_set_mock(A::class, mockA::class);
(new A)->who();
?>
```

Результат виконання цього прикладу:

```
mockA
```

**Приклад #2 Приклад використання **uopzsetmock()****

```php
<?php
class A {
    public function who() {
        echo "A";
    }
}

uopz_set_mock(A::class, new class {
                            public function who() {
                                echo "mockA";
                            }
                        });
(new A)->who();
?>
```

Результат виконання цього прикладу:

```
mockA
```

**Приклад #3 **uopzsetmock()** та статичні члени класу**

Починаючи з uopz 6.0.0, імітація статичних членів класу не підтримується.

```php
<?php
class A {
    public static function who() {
        echo "A";
    }
}

uopz_set_mock(A::class, new class {
                            const CON = 'mockA';
                            public static function who() {
                                echo "mockA";
                            }
                        });
echo A::CON, PHP_EOL;
A::who();
```

Результат виконання цього прикладу:

```
A
A
```

Висновок прикладу uopz 5:

```
mockA
mockA
```

### Дивіться також

-   [uopz\_get\_mock()](function.uopz-get-mock.html) - отримати поточний імітатор (mock) для класу
-   [uopz\_unset\_mock()](function.uopz-unset-mock.html) - Видалити раніше встановлений імітатор