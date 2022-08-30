Перевіряє, чи текст містить підозрілі символи

-   [« Spoofchecker::construct](spoofchecker.construct.html)
    
-   [Spoofchecker::setAllowedLocales »](spoofchecker.setallowedlocales.html)
    
-   [PHP Manual](index.html)
    
-   [Spoofchecker](class.spoofchecker.html)
    
-   Перевіряє, чи текст містить підозрілі символи
    

# Spoofchecker::isSuspicious

(PHP 5 >= 5.4.0, PHP 7, PHP 8, PECL intl >= 2.0.0)

Spoofchecker::isSuspicious — Перевіряє, чи текст містить підозрілі символи

### Опис

```methodsynopsis
public Spoofchecker::isSuspicious(string $string, int &$errorCode = null): bool
```

Перевіряє, чи текст містить підозрілі символи, які візуально ідентичні, але є символами Unicode з іншого мовного набору.

### Список параметрів

`string`

Рядок для перевірки.

`errorCode`

Цей параметр передається за посиланням та заповнюється цілим числом (int), що містить помилку, якщо така є.

### Значення, що повертаються

Повертає **`true`**, якщо містить підозрілі символи та **`false`**, якщо ні.

### Приклади

**Приклад #1 Приклад використання **Spoofchecker::isSuspicious()****

```php
<?php
$checker = new Spoofchecker();

$checker->isSuspicious('google.com'); // false: только символы ASCII

$checker->isSuspicious('Рaypal.com'); // true
// Первая буква из кириллического набора, а не обычная латинская "P"
```