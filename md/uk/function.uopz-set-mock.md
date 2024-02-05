---
navigation:
  - function.uopz-set-hook.md: « uopz\_set\_hook
  - function.uopz-set-property.md: uopz\_set\_property »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_set\_mock
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_set\_mock

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopz\_set\_mock — Використовувати імітатор замість класу для нових об'єктів

### Опис

```methodsynopsis
uopz_set_mock(string $class, mixed $mock): void
```

Якщо `mock` - це рядок, що містить ім'я класу, тоді він буде створений замість `class`. . `mock` також може бути об'єктом.

> **Зауваження** :
> 
> Тільки динамічний доступ до властивостей та методів буде використовувати об'єкт `mock`. Статичний доступ використовуватиме оригінальний `class`Смотрите[приклад](function.uopz-set-mock.md#uopz_set_mock.example.static) нижче.

### Список параметрів

`class`

Ім'я класу, який буде імітовано.

`mock`

Імітатор у вигляді рядка, що містить ім'я класу, що використовується, або об'єкт. Якщо передано рядок, він має містити абсолютне ім'я класу. У цьому випадку рекомендується використовувати магічну константу `::class`

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Опис |
| --- | --- |
| uopz 6.0.0 | Імітування статичних функцій не підтримуються цієї функцією. Замість цього слід використовувати [uopz\_redefine()](function.uopz-redefine.md) і [uopz\_set\_return()](function.uopz-set-return.md), или[Componere](book.componere.md) |

### Приклади

**Приклад #1 Приклад використання** uopz\_set\_mock()\*\*\*\*

```php
<?php
class A {
    public function who() {
        echo "A";
    }
}

class mockA {
    public function who() {
        echo "mockA";
    }
}

uopz_set_mock(A::class, mockA::class);
(new A)->who();
?>
```

Результат виконання наведеного прикладу:

```
mockA
```

**Приклад #2 Приклад використання** uopz\_set\_mock()\*\*\*\*

```php
<?php
class A {
    public function who() {
        echo "A";
    }
}

uopz_set_mock(A::class, new class {
                            public function who() {
                                echo "mockA";
                            }
                        });
(new A)->who();
?>
```

Результат виконання наведеного прикладу:

```
mockA
```

**Приклад #3**uopz\_set\_mock()\*\* та статичні члени класу\*\*

Починаючи з uopz 6.0.0, імітація статичних членів класу не підтримується.

```php
<?php
class A {
    public static function who() {
        echo "A";
    }
}

uopz_set_mock(A::class, new class {
                            const CON = 'mockA';
                            public static function who() {
                                echo "mockA";
                            }
                        });
echo A::CON, PHP_EOL;
A::who();
```

Результат виконання наведеного прикладу:

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

-   [uopz\_get\_mock()](function.uopz-get-mock.md) \- отримати поточний імітатор (mock) для класу
-   [uopz\_unset\_mock()](function.uopz-unset-mock.md) \- Видалити раніше встановлений імітатор
