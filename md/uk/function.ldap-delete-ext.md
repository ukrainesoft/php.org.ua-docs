---
navigation:
  - function.ldap-count-references.md: « ldap\_count\_references
  - function.ldap-delete.md: ldap\_delete »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_delete\_ext
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_delete\_ext

(PHP 7 >= 7.3.0, PHP 8)

ldap\_delete\_ext — Видалити запис із директорії

### Опис

```methodsynopsis
ldap_delete_ext(LDAP\Connection $ldap, string $dn, ?array $controls = null): LDAP\Result|false
```

Робить те саме, що й [ldap\_delete()](function.ldap-delete.md), але повертає екземпляр [LDAP\\Result](class.ldap-result.md)для разбора с помощью[ldap\_parse\_result()](function.ldap-parse-result.md)

### Список параметрів

Смотрите[ldap\_delete()](function.ldap-delete.md)

### Значення, що повертаються

Повертає екземпляр [LDAP\\Result](class.ldap-result.md)или\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.1.0 | Повертає екземпляр [LDAP\\Result](class.ldap-result.md); раніше повертався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |

### Дивіться також

-   [ldap\_delete()](function.ldap-delete.md) \- Видаляє запис із директорії LDAP
-   [ldap\_parse\_result()](function.ldap-parse-result.md) \- Витягти інформацію з результату
