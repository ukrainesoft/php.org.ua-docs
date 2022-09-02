---
navigation:
  - function.ldap-t61-to-8859.md: « ldapt61то
  - class.ldap-connection.md: LDAPConnection »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapunbind
---
# ldapunbind

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapunbind — Розірвати прив'язку до директорії LDAP

### Опис

```methodsynopsis
ldap_unbind(LDAP\Connection $ldap): bool
```

Розриває прив'язку до LDAP-директорії.

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.md), що повертається функцією [ldapconnect()](function.ldap-connect.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [ldapbind()](function.ldap-bind.md) - Прив'язати до LDAP директорії
