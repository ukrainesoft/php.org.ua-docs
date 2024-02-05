---
navigation:
  - function.ldap-exop-sync.md: « ldap\_exop\_sync
  - function.ldap-exop.md: ldap\_exop »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_exop\_whoami
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_exop\_whoami

(PHP 7 >= 7.2.0, PHP 8)

ldap\_exop\_whoami — Обертка для розширеної операції WHOAMI

### Опис

```methodsynopsis
ldap_exop_whoami(LDAP\Connection $ldap): string|false
```

Виконує розширену операцію WHOAMI та повертає дані.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

### Значення, що повертаються

Дані, повернуті сервером, або **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |

### Дивіться також

-   [ldap\_exop()](function.ldap-exop.md) \- Виконує розширену операцію
