---
navigation:
  - function.ldap-count-entries.md: « ldapcountentries
  - function.ldap-delete-ext.md: ldapdeleteext »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapcountreferences
---
# ldapcountreferences

(PHP 8)

ldapcountreferences — Підраховує кількість посилань у результатах пошуку

### Опис

```methodsynopsis
ldap_count_references(LDAP\Connection $ldap, LDAP\Result $result): int
```

Підраховує кількість посилань у результатах пошуку.

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.md), що повертається функцією [ldapconnect()](function.ldap-connect.md)

`result`

Екземпляр [LDAPResult](class.ldap-result.md), що повертається [ldaplist()](function.ldap-list.md) або [ldapsearch()](function.ldap-search.md)

### Значення, що повертаються

Повертає кількість посилань у результаті пошуку.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | Параметр `result` тепер чекає екземпляр [LDAPResult](class.ldap-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [ldapconnect()](function.ldap-connect.md) - Підключитись до сервера LDAP
