Перевірити, чи є рядки підозрілими

-   [« Spoofchecker](class.spoofchecker.html)
    
-   [Spoofchecker::construct »](spoofchecker.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Spoofchecker](class.spoofchecker.html)
    
-   Перевірити, чи є рядки підозрілими
    

# Spoofchecker::areConfusable

(PHP 5 >= 5.4.0, PHP 7, PHP 8, PECL intl >= 2.0.0)

Spoofchecker::areConfusable — Перевірити, чи є рядки підозрілими

### Опис

```methodsynopsis
public Spoofchecker::areConfusable(string $string1, string $string2, int &$errorCode = null): bool
```

Перевіряє, наскільки легко переплутати два рядки.

### Список параметрів

`string1`

Перший рядок.

`string2`

Другий рядок.

`errorCode`

Цей параметр передається за посиланням та заповнюється цілим числом (int), що містить помилку, якщо така є.

### Значення, що повертаються

Повертає **`true`**, якщо два рядки легко переплутати та **`false`**, якщо ні.

### Приклади

**Приклад #1 Приклад використання **Spoofchecker::areConfusable()****

```php
<?php
$checker = new Spoofchecker();

$checker->areConfusable('google.com', 'goog1e.com'); // true
// Английскую строчную "l" легко перепутать с цифрой 1

$checker->areConfusable('google.com', 'g00g1e.com'); // false
// Ноль (0) сложно перепутать со строчной "o"
```