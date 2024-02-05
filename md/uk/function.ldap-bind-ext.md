---
navigation:
  - function.ldap-add.md: « ldap\_add
  - function.ldap-bind.md: ldap\_bind »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_bind\_ext
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_bind\_ext

(PHP 7 >= 7.3.0, PHP 8)

ldap\_bind\_ext — Прив'язати до директорії LDAP

### Опис

```methodsynopsis
ldap_bind_ext(    LDAP\Connection $ldap,    ?string $dn = null,    ?string $password = null,    ?array $controls = null): LDAP\Result|false
```

Робить те саме, що й [ldap\_bind()](function.ldap-bind.md), але повертає екземпляр [LDAP\\Result](class.ldap-result.md)для разбора с помощью[ldap\_parse\_result()](function.ldap-parse-result.md)

### Список параметрів

Смотрите[ldap\_bind()](function.ldap-bind.md)

### Значення, що повертаються

Повертає екземпляр [LDAP\\Result](class.ldap-result.md)или\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.1.0 | Повертає екземпляр [LDAP\\Result](class.ldap-result.md); раніше повертався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |

### Дивіться також

-   [ldap\_bind()](function.ldap-bind.md) \- Прив'язати до LDAP директорії
-   [ldap\_parse\_result()](function.ldap-parse-result.md) \- Витягти інформацію з результату
