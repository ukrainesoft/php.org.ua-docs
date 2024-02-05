---
navigation:
  - function.ldap-exop-refresh.md: « ldap\_exop\_refresh
  - function.ldap-exop-whoami.md: ldap\_exop\_whoami »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_exop\_sync
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_exop\_sync

(PHP 8 >= 8.3.0)

ldap\_exop\_sync — Виконує розширену операцію

### Опис

```methodsynopsis
ldap_exop_sync(    LDAP\Connection $ldap,    string $request_oid,    string $request_data = null,    array $controls = null,    string &$response_data = null,    string &$response_oid = null): LDAP\Result|bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`request_oid`

`request_data`

`controls`

`response_data`

`response_oid`

### Значення, що повертаються

### Дивіться також

-   [ldap\_exop()](function.ldap-exop.md) \- Виконує розширену операцію
