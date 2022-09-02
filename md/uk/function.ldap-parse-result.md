---
navigation:
  - function.ldap-parse-reference.md: « ldapparsereference
  - function.ldap-read.md: ldapread »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapparseresult
---
# ldapparseresult

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

ldapparseresult — Витягти інформацію з результату

### Опис

```methodsynopsis
ldap_parse_result(    LDAP\Connection $ldap,    LDAP\Result $result,    int &$error_code,    string &$matched_dn = null,    string &$error_message = null,    array &$referrals = null,    array &$controls = null): bool
```

Обробляє результат пошуку LDAP.

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.md), що повертається функцією [ldapconnect()](function.ldap-connect.md)

`result`

Екземпляр [LDAPResult](class.ldap-result.md), що повертається [ldaplist()](function.ldap-list.md) або [ldapsearch()](function.ldap-search.md)

`error_code`

Посилання на змінну, якій надається код помилки LDAP, або `0`якщо немає помилки.

`matched_dn`

Посилання на змінну, якій надається знайдений DN, якщо він визначається в запиті, інакше присвоюється **`null`**

`error_message`

Посилання на змінну, якій присвоюється повідомлення про помилку LDAP, або порожній рядок, якщо немає помилки.

`referrals`

Посилання на змінну, якій присвоюється масив (array) з усіма посиланнями (referral) як рядків, чи порожній масив, якщо вони повернули.

`controls`

Масив (array) LDAP Controls, які були відправлені замість відповіді.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | Параметр `result` тепер чекає екземпляр [LDAPResult](class.ldap-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | Додано підтримку параметра `controls` |

### Приклади

**Приклад #1 Приклад використання **ldapparseresult()****

```php
<?php
$result = ldap_search($ldap, "cn=userref,dc=my-domain,dc=com", "(cn=user*)");
$errcode = $dn = $errmsg = $refs =  null;
if (ldap_parse_result($ldap, $result, $errcode, $dn, $errmsg, $refs)) {
    // различные операции с $errcode, $dn, $errmsg и $refs
}
?>
```
