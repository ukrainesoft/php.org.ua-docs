---
navigation:
  - function.ldap-get-attributes.md: « ldapgetattributes
  - function.ldap-get-entries.md: ldapgetentries »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapgetдн
---
# ldapgetдн

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapgetdn — Отримати DN результуючого запису

### Опис

```methodsynopsis
ldap_get_dn(LDAP\Connection $ldap, LDAP\ResultEntry $entry): string|false
```

Виявити DN запису в результаті.

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.md), що повертається функцією [ldapconnect()](function.ldap-connect.md)

`entry`

Екземпляр [LDAPResultEntry](class.ldap-result-entry.md)

### Значення, що повертаються

Повертає DN запису результату та **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | Параметр `entry` тепер чекає екземпляр [LDAPResultEntry](class.ldap-result-entry.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
