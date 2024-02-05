---
navigation:
  - function.token-get-all.md: « token\_get\_all
  - book.url.md: URL »
  - index.md: PHP Manual
  - ref.tokenizer.md: Функції PHP-лексера (tokenizer)
title: token\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# token\_name

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

token\_name — Отримати символьне ім'я для переданої PHP-лексеми

### Опис

```methodsynopsis
token_name(int $id): string
```

Функция**token\_name()** отримує символьне ім'я для значення PHP-лексеми `id`

### Список параметрів

`id`

Значення лексеми.

### Значення, що повертаються

Символьне значення для переданої лексеми `id`

### Приклади

**Пример #1 Пример использования**token\_name()\*\*\*\*

```php
<?php
// 260 - значение для лексемы T_EVAL
echo token_name(260);        // -> "T_EVAL"

// Константа лексемы сопоставима с его собственным именем
echo token_name(T_FUNCTION); // -> "T_FUNCTION"
?>
```

### Дивіться також

-   [Список лексем](tokens.md)
-   [PhpToken::getTokenName()](phptoken.gettokenname.md) \- Повертає ім'я токена
