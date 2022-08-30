Екранує рядок за допомогою слішів

-   [« addcslashes](function.addcslashes.html)
    
-   [bin2hex »](function.bin2hex.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з рядками](ref.strings.html)
    
-   Екранує рядок за допомогою слішів
    

# addslashes

(PHP 4, PHP 5, PHP 7, PHP 8)

addslashes — Екранує рядок за допомогою слішів

### Опис

```methodsynopsis
addslashes(string $string): string
```

Повертає рядок зі зворотним слішем перед символами, які потрібно екранувати. Екрануються такі символи:

-   одинарна лапка (`'`
-   подвійна лапка (`"`
-   зворотний сліш (`\`
-   NUL (байт **`null`**

Невеликий приклад використання функції **addslashes()** для екранування перелічених вище символів:

```php
<?php
$str = "O'Reilly?";
eval("echo '" . addslashes($str) . "';");
?>
```

Іноді функцію **addslashes()** некоректно намагаються використати для запобігання [SQL-инъекций](security.database.sql-injection.html). Чи не робіть так. Замість цього використовуйте підготовлені запити або функції екранування відповідних модулів роботи з базами даних.

### Список параметрів

`string`

Рядок, що екранується.

### Значення, що повертаються

Повертає рядок, що екранується.

### Приклади

**Приклад #1 Приклад використання **addslashes()****

```php
<?php
$str = "Ваше имя O'Reilly?";

// выводит: Ваше имя O\'Reilly?
echo addslashes($str);
?>
```

### Дивіться також

-   [stripcslashes()](function.stripcslashes.html) - Видаляє екранування символів, зроблене функцією addcslashes
-   [stripslashes()](function.stripslashes.html) - Видаляє екранування символів
-   [addcslashes()](function.addcslashes.html) - Екранує рядок слішами у стилі мови C
-   [htmlspecialchars()](function.htmlspecialchars.html) - Перетворює спеціальні символи на HTML-сутності
-   [quotemeta()](function.quotemeta.html) - Екранує спеціальні символи
-   [getmagicquotesgpc()](function.get-magic-quotes-gpc.html) - Отримання поточного значення конфігурації конфігурації magicquotesgpc