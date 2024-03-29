---
navigation:
  - phptoken.tostring.md: '« PhpToken::\_\_function toString() { [native code] }'
  - ref.tokenizer.md: Функції PHP-лексера (tokenizer) »
  - index.md: PHP Manual
  - class.phptoken.md: PhpToken
title: 'PhpToken::tokenize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PhpToken::tokenize

(PHP 8)

PhpToken::tokenize — Розбирає заданий рядок, що містить програму на PHP, на масив об'єктів PhpToken

### Опис

```methodsynopsis
public static PhpToken::tokenize(string $code, int $flags = 0): array
```

Повертає масив об'єктів PhpToken, які представляють код `code`

### Список параметрів

`code`

Вихідний код мовою PHP.

`flags`

Допустимі прапори:

-   \*\*`TOKEN_PARSE`\*\*- Допускає можливість використовувати зарезервовані слова у певних контекстах.

### Значення, що повертаються

Масив токенів PHP як об'єктів класу PhpToken чи його нащадків. Цей метод повертає static\[\]так що PhpToken можна вільно розширювати.

### Приклади

**Приклад #1 Приклад використання** PhpToken::tokenize()\*\*\*\*

```php
<?php
$tokens = PhpToken::tokenize('<?php echo; ?>');

foreach ($tokens as $token) {
    echo "Line {$token->line}: {$token->getTokenName()} ('{$token->text}')", PHP_EOL;
}
```

Результат виконання наведених прикладів:

```
Line 1: T_OPEN_TAG ('<?php ')
Line 1: T_ECHO ('echo')
Line 1: ; (';')
Line 1: T_WHITESPACE (' ')
Line 1: T_CLOSE_TAG ('?>')
```

**Приклад #2 Розширення PhpToken**

```php
<?php

class MyPhpToken extends PhpToken {
    public function getUpperText() {
        return strtoupper($this->text);
    }
}

$tokens = MyPhpToken::tokenize('<?php echo; ?>');
echo "'{$tokens[0]->getUpperText()}'";
```

Результат виконання наведених прикладів:

```
'<?PHP '
```

### Дивіться також

-   [token\_get\_all()](function.token-get-all.md) \- Розбиває переданий вихідний код на PHP-лексеми
