---
navigation:
  - function.ldap-next-reference.md: « ldapnextreference
  - function.ldap-parse-reference.md: ldapparsereference »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapparseexop
---
# ldapparseexop

(PHP 7> = 7.2.0, PHP 8)

ldapparseexop — Розбір результуючого об'єкта виконання розширеної операції LDAP

### Опис

```methodsynopsis
ldap_parse_exop(    LDAP\Connection $ldap,    LDAP\Result $result,    string &$response_data = null,    string &$response_oid = null): bool
```

Розбирає `result`отриманий після виконання розширеної операції LDAP

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.md), що повертається функцією [ldapconnect()](function.ldap-connect.md)

`result`

Екземпляр [LDAPResult](class.ldap-result.md), що повертається [ldaplist()](function.ldap-list.md) або [ldapsearch()](function.ldap-search.md)

`response_data`

Буде заповнений розібраними даними.

`response_oid`

Буде заповнено поверненим OID.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | Параметр `result` тепер чекає екземпляр [LDAPResult](class.ldap-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [ldapexop()](function.ldap-exop.md) - Виконує розширену операцію
