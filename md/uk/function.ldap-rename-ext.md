---
navigation:
  - function.ldap-read.md: « ldap\_read
  - function.ldap-rename.md: ldap\_rename »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_rename\_ext
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_rename\_ext

(PHP 7 >= 7.3.0, PHP 8)

ldap\_rename\_ext — Модифікувати назву запису

### Опис

```methodsynopsis
ldap_rename_ext(    LDAP\Connection $ldap,    string $dn,    string $new_rdn,    string $new_parent,    bool $delete_old_rdn,    ?array $controls = null): LDAP\Result|false
```

Робить те саме, що й [ldap\_rename()](function.ldap-rename.md), але повертає екземпляр [LDAP\\Result](class.ldap-result.md)для разбора с помощью[ldap\_parse\_result()](function.ldap-parse-result.md)

### Список параметрів

Смотрите[ldap\_rename()](function.ldap-rename.md)

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

-   [ldap\_rename()](function.ldap-rename.md) \- Змінити ім'я запису
-   [ldap\_parse\_result()](function.ldap-parse-result.md) \- Витягти інформацію з результату
