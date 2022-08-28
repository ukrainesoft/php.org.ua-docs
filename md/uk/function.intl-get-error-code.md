Отримати код останньої помилки

-   [« intl\_error\_name](function.intl-error-name.html)
    
-   [intl\_get\_error\_message »](function.intl-get-error-message.html)
    
-   [PHP Manual](index.html)
    
-   [Функции intl](ref.intl.html)
    
-   Отримати код останньої помилки
    

# intlgeterrorcode

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

intlgeterrorcode — Отримати код останньої помилки

### Опис

```methodsynopsis
intl_get_error_code(): int
```

Корисно для обробки помилок статичних методів, коли немає об'єкта для вилучення помилки з нього.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Код помилки, повернутий останнім викликом функції API.

### Приклади

**Приклад #1 Приклад використання **intlgeterrorcode()****

```php
<?php
$coll = collator_create( '<bad_param>' );
if( !$coll ) {
    handle_error( intl_get_error_code() );
}
?>
```

### Дивіться також

-   [intl\_is\_failure()](function.intl-is-failure.html) - Перевірити, чи є код помилки ознакою збою
-   [intl\_error\_name()](function.intl-error-name.html) - Отримати ім'я помилки за її кодом
-   [intl\_get\_error\_message()](function.intl-get-error-message.html) - Отримати опис помилки
-   [collator\_get\_error\_code()](collator.geterrorcode.html) - Отримує останній код помилки Collator
-   [numfmt\_get\_error\_code()](numberformatter.geterrorcode.html) - Отримує останній код помилки засобу форматування