---
navigation:
  - function.mailparse-msg-parse.md: « mailparse\_msg\_parse
  - function.mailparse-stream-encode.md: mailparse\_stream\_encode »
  - index.md: PHP Manual
  - ref.mailparse.md: Mailparse
title: mailparse\_rfc822\_parse\_addresses
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mailparse\_rfc822\_parse\_addresses

(PECL mailparse >= 0.9.0)

mailparse\_rfc822\_parse\_addresses — Розібрати адреси відповідно до RFC 822

### Опис

```methodsynopsis
mailparse_rfc822_parse_addresses(string $addresses): array
```

Розбирає список одержувачів відповідно до [» RFC 822](http://www.faqs.org/rfcs/rfc822). Список одержувачів зазвичай знаходиться у заголовку `To:`

### Список параметрів

`addresses`

Рядок, що містить адреси. Наприклад: `Wez Furlong <wez@example.com>, doe@example.com`

> **Зауваження** :
> 
> Цей рядок не повинен містити назву заголовка.

### Значення, що повертаються

Повертає асоціативний масив кожного одержувача з такими ключами:

< td>**`true`**, якщо одержувач є групою розсилки та **`false`**, якщо ні.

<table class="doctable informaltable"><tbody class="tbody"><tr><td><code class="literal">display</code></td><td>Ім'я одержувача. Якщо ця частина адреси не задана, то буде використано те саме значення, що й для <code class="literal">address</code>.</td></tr><tr><td><code class=" literal">address</code></td><td>Адреса електронної пошти</td></tr><tr><td><code class="literal">is_group</code></td></tr></tbody></table>

### Приклади

**Пример #1 Пример использования**mailparse\_rfc822\_parse\_addresses()\*\*\*\*

```php
<?php

$to = 'Wez Furlong <wez@example.com>, doe@example.com';
var_dump(mailparse_rfc822_parse_addresses($to));

?>
```

Результат виконання наведеного прикладу:

```
array(2) {
  [0]=>
  array(3) {
    ["display"]=>
    string(11) "Wez Furlong"
    ["address"]=>
    string(15) "wez@example.com"
    ["is_group"]=>
    bool(false)
  }
  [1]=>
  array(3) {
    ["display"]=>
    string(15) "doe@example.com"
    ["address"]=>
    string(15) "doe@example.com"
    ["is_group"]=>
    bool(false)
  }
}
```
