---
navigation:
  - function.ldap-next-reference.md: « ldap\_next\_reference
  - function.ldap-parse-reference.md: ldap\_parse\_reference »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_parse\_exop
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_parse\_exop

(PHP 7 >= 7.2.0, PHP 8)

ldap\_parse\_exop — Розбір результуючого об'єкта виконання розширеної операції LDAP

### Опис

```methodsynopsis
ldap_parse_exop(    LDAP\Connection $ldap,    LDAP\Result $result,    string &$response_data = null,    string &$response_oid = null): bool
```

Розбирає `result`отриманий після виконання розширеної операції LDAP

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`result`

Екземпляр [LDAP\\Result](class.ldap-result.md), що повертається [ldap\_list()](function.ldap-list.md) або [ldap\_search()](function.ldap-search.md)

`response_data`

Буде заповнений розібраними даними.

`response_oid`

Буде заповнено поверненим OID.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [LDAP\\Result](class.ldap-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap result` |

### Дивіться також

-   [ldap\_exop()](function.ldap-exop.md) \- Виконує розширену операцію
