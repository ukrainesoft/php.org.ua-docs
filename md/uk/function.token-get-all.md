---
navigation:
  - ref.tokenizer.md: Функції PHP-лексера (tokenizer)
  - function.token-name.md: token\_name »
  - index.md: PHP Manual
  - ref.tokenizer.md: Функції PHP-лексера (tokenizer)
title: token\_get\_all
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# token\_get\_all

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

token\_get\_all — Розбиває переданий вихідний код на PHP-лексеми

### Опис

```methodsynopsis
token_get_all(string $code, int $flags = 0): array
```

Функция**token\_get\_all()** розбирає переданий рядок `code` у мовні лексеми PHP, використовуючи лексичний сканер Zend Engine.

Список лексем смотрите в[Список тегів (tokens) парсера](tokens.md)или используйте[token\_name()](function.token-name.md) для переведення значення лексеми в рядкову виставу.

### Список параметрів

`code`

Вихідний код PHP для аналізу.

`flags`

Коректні прапори:

-   \*\*`TOKEN_PARSE`\*\*- Визначає можливість використання зарезервованих слів у певних контекстах.

### Значення, що повертаються

Масив ідентифікаторів лексем. Кожен індивідуальний ідентифікатор лексеми це чи одиночний символ (наприклад, `>` `!`, інші...), або триелементний масив, що містить індекс лексеми в нульовому елементі, рядок з оригінальним вмістом лексеми у першому елементі та номером рядка у другому елементі.

### Приклади

**Приклад #1**token\_get\_all()**example**

```php
<?php
$tokens = token_get_all('<?php echo; ?>');

foreach ($tokens as $token) {
    if (is_array($token)) {
        echo "Строка {$token[2]}: ", token_name($token[0]), " ('{$token[1]}')", PHP_EOL;
    }
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Строка 1: T_OPEN_TAG ('<?php ')
Строка 1: T_ECHO ('echo')
Строка 1: T_WHITESPACE (' ')
Строка 1: T_CLOSE_TAG ('?>')
```

**Приклад #2 Приклад неправильного использования**token\_get\_all()\*\*\*\*

```php
<?php
$tokens = token_get_all('/* комментарий */');

foreach ($tokens as $token) {
    if (is_array($token)) {
        echo "Строка {$token[2]}: ", token_name($token[0]), " ('{$token[1]}')", PHP_EOL;
    }
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Строка 1: T_INLINE_HTML ('/* комментарий */')
```

Зверніть увагу, у наведеному прикладі рядок розбирається як **`T_INLINE_HTML`** замість очікуваного **`T_COMMENT`**. Це пов'язано з тим, що не використовується тег, що відкриває в коді. Це було б еквівалентно розміщенню коментарів поза тегами PHP у звичайному файлі.

**Приклад #3 Приклад використання** token\_get\_all()\*\* з класом, який використовує зарезервовані слова\*\*

```php
<?php

$source = <<<'code'
<?php

class A
{
    const PUBLIC = 1;
}
code;

$tokens = token_get_all($source, TOKEN_PARSE);

foreach ($tokens as $token) {
    if (is_array($token)) {
        echo token_name($token[0]) , PHP_EOL;
    }
}
?>
```

Висновок наведеного прикладу буде схожим на:

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

Без флага\*\*`TOKEN_PARSE`**, передостанній токен (**`T_STRING`\*\*) був би **`T_PUBLIC`**

### Дивіться також

-   [PhpToken::tokenize()](phptoken.tokenize.md) \- Розбирає заданий рядок, що містить програму на PHP, на масив об'єктів PhpToken
-   [token\_name()](function.token-name.md) \- Отримати символьне ім'я для переданої PHP-лексеми
