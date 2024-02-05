---
navigation:
  - function.ldap-get-attributes.md: « ldap\_get\_attributes
  - function.ldap-get-entries.md: ldap\_get\_entries »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_get\_dn
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_get\_dn

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap\_get\_dn — Отримати DN результуючого запису

### Опис

```methodsynopsis
ldap_get_dn(LDAP\Connection $ldap, LDAP\ResultEntry $entry): string|false
```

Виявити DN запису в результаті.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`entry`

Екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.md)

### Значення, що повертаються

Возвращает DN записи результата и\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.1.0 | Параметр`entry` тепер чекає екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap result entry` |
