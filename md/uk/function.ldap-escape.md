---
navigation:
  - function.ldap-error.md: « ldaperror
  - function.ldap-exop-passwd.md: ldapexoppasswd »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapescape
---
# ldapescape

(PHP 5> = 5.6.0, PHP 7, PHP 8)

ldapescape — Екранування рядка для використання у фільтрі LDAP або DN

### Опис

```methodsynopsis
ldap_escape(string $value, string $ignore = "", int $flags = 0): string
```

Екранує `value` для використання в контексті заданому в `flags`

### Список параметрів

`value`

Значення екранування.

`ignore`

Символи, які потрібно ігнорувати під час екранування.

`flags`

Контекст, для якого екранується рядок: **`LDAP_ESCAPE_FILTER`** для фільтрів, що використовуються в [ldapsearch()](function.ldap-search.md) або **`LDAP_ESCAPE_DN`** для DN. Якщо не передані жодні прапори, всі символи будуть екрановані.

### Значення, що повертаються

повертає екранований рядок.

### Приклади

При побудові фільтра LDAP ви повинні використовувати ldapescape з прапором LDAPESCAPEFILTER.

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
