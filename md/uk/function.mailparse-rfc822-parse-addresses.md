---
navigation:
  - function.mailparse-msg-parse.html: « mailparsemsgparse
  - function.mailparse-stream-encode.html: mailparsestreamencode »
  - index.html: PHP Manual
  - ref.mailparse.html: Mailparse
title: mailparserfc822parseaddresses
---
# mailparserfc822parseaddresses

(PECL mailparse >= 0.9.0)

mailparserfc822parseaddresses — Розібрати адреси відповідно до RFC 822

### Опис

```methodsynopsis
mailparse_rfc822_parse_addresses(string $addresses): array
```

Розбирає список одержувачів відповідно до [» RFC 822](http://www.faqs.org/rfcs/rfc822). Список одержувачів зазвичай знаходиться у заголовку `To:`

### Список параметрів

`addresses`

Рядок, що містить адреси. Наприклад: `Wez Furlong <wez@example.com>, doe@example.com`

> **Зауваження**
> 
> Цей рядок не повинен містити назву заголовка.

### Значення, що повертаються

Повертає асоціативний масив кожного одержувача з такими ключами:

< td>**`true`**, якщо одержувач є групою розсилки та **`false`**, якщо ні.

<table class="doctable informaltable"><tbody class="tbody"><tr><td><code class="literal">display</code></td><td>Ім'я одержувача. Якщо ця частина адреси не задана, то буде використано те саме значення, що й для <code class="literal">address</code>.</td></tr><tr><td><code class=" literal">address</code></td><td>Адреса електронної пошти</td></tr><tr><td><code class="literal">is_group</code></td></tr></tbody></table>

### Приклади

**Приклад #1 Приклад використання **mailparserfc822parseaddresses()****

```php
<?php

$to = 'Wez Furlong <wez@example.com>, doe@example.com';
var_dump(mailparse_rfc822_parse_addresses($to));

?>
```

Результат виконання цього прикладу:

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
