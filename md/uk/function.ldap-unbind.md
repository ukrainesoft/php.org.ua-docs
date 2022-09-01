---
navigation:
  - function.ldap-t61-to-8859.html: « ldapt61то
  - class.ldap-connection.html: LDAPConnection »
  - index.html: PHP Manual
  - ref.ldap.html: Функції LDAP
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

Екземпляр [LDAPConnection](class.ldap-connection.html), що повертається функцією [ldapconnect()](function.ldap-connect.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [ldapbind()](function.ldap-bind.html) - Прив'язати до LDAP директорії
