---
navigation:
  - function.ldap-exop-refresh.md: « ldapexoprefresh
  - function.ldap-exop.md: ldapexop »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapexopwhoami
---
# ldapexopwhoami

(PHP 7> = 7.2.0, PHP 8)

ldapexopwhoami — Обертка для розширеної операції WHOAMI

### Опис

```methodsynopsis
ldap_exop_whoami(LDAP\Connection $ldap): string|false
```

Виконує розширену операцію WHOAMI та повертає дані.

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.md), що повертається функцією [ldapconnect()](function.ldap-connect.md)

### Значення, що повертаються

Дані, повернуті сервером, або **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [ldapexop()](function.ldap-exop.md) - Виконує розширену операцію
