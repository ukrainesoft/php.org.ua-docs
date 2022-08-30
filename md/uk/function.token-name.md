Отримати символьне ім'я для переданої PHP-лексеми

-   [« tokengetall](function.token-get-all.html)
    
-   [URL »](book.url.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PHP-лексера (tokenizer)](ref.tokenizer.html)
    
-   Отримати символьне ім'я для переданої PHP-лексеми
    

# tokenname

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

tokenname — Отримати символьне ім'я для переданої PHP-лексеми

### Опис

```methodsynopsis
token_name(int $id): string
```

Функція **tokenname()** отримує символьне ім'я для значення PHP-лексеми `id`

### Список параметрів

`id`

Значення лексеми.

### Значення, що повертаються

Символьне значення для переданої лексеми `id`

### Приклади

**Приклад #1 Приклад використання **tokenname()****

```php
<?php
// 260 - значение для лексемы T_EVAL
echo token_name(260);        // -> "T_EVAL"

// Константа лексемы сопоставима с его собственным именем
echo token_name(T_FUNCTION); // -> "T_FUNCTION"
?>
```

### Дивіться також

-   [Список лексем](tokens.html)
-   [PhpToken::getTokenName()](phptoken.gettokenname.html) - Повертає ім'я токена