---
navigation:
  - function.uopz-redefine.md: « uopz\_redefine
  - function.uopz-restore.md: uopz\_restore »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_rename
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_rename

(PECL uopz 1, PECL uopz 2)

uopz\_rename — Перейменувати функцію під час виконання

**Увага**

Ця функція була *ВИДАЛЕНО*в PECL uopz 5.0.0.

### Опис

```methodsynopsis
uopz_rename(string $function, string $rename): void
```

```methodsynopsis
uopz_rename(string $class, string $function, string $rename): void
```

Перейменовує функцію `function`на`rename`

> **Зауваження** :
> 
> Якщо обидві функції існують, ця функція по суті змінює імена

### Список параметрів

`class`

Ім'я класу, що містить функцію

`function`

Ім'я існуючої функції

`rename`

Нове ім'я функції

### Значення, що повертаються

### Приклади

**Пример #1 Пример использования**uopz\_rename()\*\*\*\*

```php
<?php
uopz_rename("strlen", "original_strlen");

echo original_strlen("Hello World");
?>
```

Висновок наведеного прикладу буде схожим на:

```
11
```

**Пример #2 Пример использования**uopz\_rename()\*\* з класом\*\*

```php
<?php
class My {
    public function strlen($arg) {
        return strlen($arg);
    }
}

uopz_rename(My::class, "strlen", "original_strlen");

echo My::original_strlen("Hello World");
?>
```

Результат виконання наведеного прикладу:

```
11
```
