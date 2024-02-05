---
navigation:
  - function.ldap-count-entries.md: « ldap\_count\_entries
  - function.ldap-delete-ext.md: ldap\_delete\_ext »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_count\_references
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_count\_references

(PHP 8)

ldap\_count\_references — Підраховує кількість посилань у результатах пошуку

### Опис

```methodsynopsis
ldap_count_references(LDAP\Connection $ldap, LDAP\Result $result): int
```

Підраховує кількість посилань у результатах пошуку.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`result`

Екземпляр [LDAP\\Result](class.ldap-result.md), що повертається [ldap\_list()](function.ldap-list.md) або [ldap\_search()](function.ldap-search.md)

### Значення, що повертаються

Повертає кількість посилань у результаті пошуку.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [LDAP\\Result](class.ldap-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap result` |

### Дивіться також

-   [ldap\_connect()](function.ldap-connect.md) \- Підключається до сервера LDAP
