---
navigation:
  - function.ldap-explode-dn.md: « ldap\_explode\_dn
  - function.ldap-first-entry.md: ldap\_first\_entry »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_first\_attribute
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_first\_attribute

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap\_first\_attribute — Повернути перший атрибут

### Опис

```methodsynopsis
ldap_first_attribute(LDAP\Connection $ldap, LDAP\ResultEntry $entry): string|false
```

Отримує перший атрибут у цьому записі. Атрибути, що залишаються, виходять послідовним викликом [ldap\_next\_attribute()](function.ldap-next-attribute.md)

Подібно до читання записів, атрибути також читаються один за одним з окремого елемента.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`entry`

Екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.md)

### Значення, що повертаються

Повертає перший атрибут у записі, у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.1.0 | Параметр`entry` тепер чекає екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap result entry` |
| 8.0.0 | Третій параметр, що не використовується `ber_identifier` більше не приймається. |

### Дивіться також

-   [ldap\_next\_attribute()](function.ldap-next-attribute.md) \- Отримати наступний атрибут із результату
-   [ldap\_get\_attributes()](function.ldap-get-attributes.md) \- Отримує атрибути із запису у результатах пошуку
