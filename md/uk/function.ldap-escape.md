---
navigation:
  - function.ldap-error.md: « ldap\_error
  - function.ldap-exop-passwd.md: ldap\_exop\_passwd »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_escape
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_escape

(PHP 5 >= 5.6.0, PHP 7, PHP 8)

ldap\_escape — Екранування рядка для використання у фільтрі LDAP або DN

### Опис

```methodsynopsis
ldap_escape(string $value, string $ignore = "", int $flags = 0): string
```

Екранує `value`для использования в контексте заданном в`flags`

### Список параметрів

`value`

Значення екранування.

`ignore`

Символи, які потрібно ігнорувати під час екранування.

`flags`

Контекст, для якого екранується рядок: **`LDAP_ESCAPE_FILTER`** для фільтрів, що використовуються в [ldap\_search()](function.ldap-search.md)или\*\*`LDAP_ESCAPE_DN`\*\* для DN. Якщо не передані жодні прапори, всі символи будуть екрановані.

### Значення, що повертаються

повертає екранований рядок.

### Приклади

При побудові фільтра LDAP ви повинні використовувати ldap\_escape з прапором LDAP\_ESCAPE\_FILTER.

**Приклад #1 Пошук по email-адресі**

```php
<?php
// $ds допустимый экземпляр LDAP\Connection

// $mail - email-адрес, предоставленный пользователем

$base   = "o=My Company, c=US";
$filter = "(mail=".ldap_escape($mail, "", LDAP_ESCAPE_FILTER).")";

$sr = ldap_search($ds, $base, $filter, array("sn", "givenname", "mail"));

$info = ldap_get_entries($ds, $sr);

echo $info["count"]." записей возвращено\n";
?>
```
