---
navigation:
  - function.ldap-t61-to-8859.md: « ldap\_t61\_to\_8859
  - class.ldap-connection.md: LDAP\\Connection »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_unbind
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_unbind

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap\_unbind — Розірвати прив'язку до директорії LDAP

### Опис

```methodsynopsis
ldap_unbind(LDAP\Connection $ldap): bool
```

Розриває прив'язку до LDAP-директорії.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |

### Дивіться також

-   [ldap\_bind()](function.ldap-bind.md) \- Прив'язати до LDAP директорії
