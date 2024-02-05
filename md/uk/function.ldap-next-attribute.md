---
navigation:
  - function.ldap-modify.md: « ldap\_modify
  - function.ldap-next-entry.md: ldap\_next\_entry »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_next\_attribute
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_next\_attribute

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap\_next\_attribute — Отримати наступний атрибут із результату

### Опис

```methodsynopsis
ldap_next_attribute(LDAP\Connection $ldap, LDAP\ResultEntry $entry): string|false
```

Повертає атрибути запису. Перший виклик **ldap\_next\_attribute()** проводиться з параметром `entry`, який повертається [ldap\_first\_attribute()](function.ldap-first-attribute.md)

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`entry`

Екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.md)

### Значення, що повертаються

Повертає наступний атрибут запису у разі успішного виконання та \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.1.0 | Параметр`entry` тепер чекає екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap result entry` |
| 8.0.0 | Третій параметр, що не використовується `ber_identifier` більше не приймається. |

### Дивіться також

-   [ldap\_get\_attributes()](function.ldap-get-attributes.md) \- Отримує атрибути із запису у результатах пошуку
