Розбиває переданий вихідний код на PHP-лексеми

-   [« Функции PHP-лексера (tokenizer)](ref.tokenizer.html)
    
-   [token\_name »](function.token-name.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PHP-лексера (tokenizer)](ref.tokenizer.html)
    
-   Розбиває переданий вихідний код на PHP-лексеми
    

# tokengetall

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

tokengetall — Розбиває переданий вихідний код на PHP-лексеми

### Опис

```methodsynopsis
token_get_all(string $code, int $flags = 0): array
```

Функція **tokengetall()** розбирає переданий рядок `code` у мовні лексеми PHP, використовуючи лексичний сканер Zend Engine.

Список лексем дивіться у [Список меток (tokens) парсера](tokens.html) або використовуйте [token\_name()](function.token-name.html) для переведення значення лексеми в рядкову виставу.

### Список параметрів

`code`

Вихідний код PHP для аналізу.

`flags`

Коректні прапори:

-   **`TOKEN_PARSE`** - Розпізнає можливість використання зарезервованих слів у певних контекстах.

### Значення, що повертаються

Масив ідентифікаторів лексем. Кожен індивідуальний ідентифікатор лексеми це чи одиночний символ (наприклад, `;` `.` `>` `!`, інші...), або триелементний масив, що містить індекс лексеми в нульовому елементі, рядок з оригінальним вмістом лексеми у першому елементі та номером рядка у другому елементі.

### Приклади

**Приклад #1 **tokengetall()** example**

```php
<?php
$tokens = token_get_all('<?php echo; ?>');

foreach ($tokens as $token) {
    if (is_array($token)) {
        echo "Строка {$token[2]}: ", token_name($token[0]), " ('{$token[1]}')", PHP_EOL;
    }
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Строка 1: T_OPEN_TAG ('<?php ')
Строка 1: T_ECHO ('echo')
Строка 1: T_WHITESPACE (' ')
Строка 1: T_CLOSE_TAG ('?>')
```

**Приклад #2 Приклад неправильного використання **tokengetall()****

```php
<?php
$tokens = token_get_all('/* комментарий */');

foreach ($tokens as $token) {
    if (is_array($token)) {
        echo "Строка {$token[2]}: ", token_name($token[0]), " ('{$token[1]}')", PHP_EOL;
    }
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Строка 1: T_INLINE_HTML ('/* комментарий */')
```

Зверніть увагу, у наведеному прикладі рядок розбирається як **`T_INLINE_HTML`** замість очікуваного **`T_COMMENT`**. Це пов'язано з тим, що не використовується тег, що відкриває в коді. Це було б еквівалентно розміщенню коментарів поза тегами PHP у звичайному файлі.

**Приклад #3 Приклад використання **tokengetall()** з класом, який використовує зарезервовані слова**

```php
<?php

$source = <<<'code'
<?php

class A
{
    const PUBLIC = 1;
}
code;

$tokens = token_get_all($source, TOKEN_PARSE);

foreach ($tokens as $token) {
    if (is_array($token)) {
        echo token_name($token[0]) , PHP_EOL;
    }
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
T_OPEN_TAG
T_WHITESPACE
T_CLASS
T_WHITESPACE
T_STRING
T_CONST
T_WHITESPACE
T_STRING
T_LNUMBER
```

Без прапора **`TOKEN_PARSE`**, передостанній токен (**`T_STRING`**) був би **`T_PUBLIC`**

### Дивіться також

-   [PhpToken::tokenize()](phptoken.tokenize.html) - Розбирає заданий рядок, що містить програму на PHP, на масив об'єктів PhpToken
-   [token\_name()](function.token-name.html) - Отримати символьне ім'я для переданої PHP-лексеми