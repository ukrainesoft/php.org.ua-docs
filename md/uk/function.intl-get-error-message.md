Отримати опис помилки

-   [« intl\_get\_error\_code](function.intl-get-error-code.html)
    
-   [intl\_is\_failure »](function.intl-is-failure.html)
    
-   [PHP Manual](index.html)
    
-   [Функции intl](ref.intl.html)
    
-   Отримати опис помилки
    

# intlgeterrormessage

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

intlgeterrormessage — Отримати опис помилки

### Опис

```methodsynopsis
intl_get_error_message(): string
```

Отримати опис останньої помилки у функціях ICU.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Опис останньої помилки у функціях ICU.

### Приклади

**Приклад #1 Приклад використання **intlgeterrormessage()****

```php
<?php
if( Collator::getAvailableLocales() === false ) {
    show_error( intl_get_error_message() );
}
?>
```

### Дивіться також

-   [intl\_error\_name()](function.intl-error-name.html) - Отримати ім'я помилки за її кодом
-   [intl\_get\_error\_code()](function.intl-get-error-code.html) - Отримати код останньої помилки
-   [intl\_is\_failure()](function.intl-is-failure.html) - Перевірити, чи є код помилки ознакою збою
-   [collator\_get\_error\_message()](collator.geterrormessage.html) - Отримує текст для останньої помилки коду Collator
-   [numfmt\_get\_error\_message()](numberformatter.geterrormessage.html) - Отримує останнє повідомлення про помилку засобу форматування