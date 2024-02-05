---
navigation:
  - function.ldap-list.md: « ldap\_list
  - function.ldap-mod-add.md: ldap\_mod\_add »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_mod\_add\_ext
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_mod\_add\_ext

(PHP 7 >= 7.3.0, PHP 8)

ldap\_mod\_add\_ext — Додати значення атрибуту до поточних атрибутів

### Опис

```methodsynopsis
ldap_mod_add_ext(    LDAP\Connection $ldap,    string $dn,    array $entry,    ?array $controls = null): LDAP\Result|false
```

Робить те саме, що й [ldap\_mod\_add()](function.ldap-mod-add.md), але повертає екземпляр [LDAP\\Result](class.ldap-result.md)для разбора с помощью[ldap\_parse\_result()](function.ldap-parse-result.md)

### Список параметрів

Смотрите[ldap\_mod\_add()](function.ldap-mod-add.md)

### Значення, що повертаються

Повертає екземпляр [LDAP\\Result](class.ldap-result.md)или\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.1.0 | Повертає екземпляр [LDAP\\Result](class.ldap-result.md); раніше повертався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |
| 7.3.0 | Додано підтримку параметра `controls` |

### Дивіться також

-   [ldap\_mod\_add()](function.ldap-mod-add.md) \- Додати значення атрибуту до поточних атрибутів
-   [ldap\_parse\_result()](function.ldap-parse-result.md) \- Витягти інформацію з результату
