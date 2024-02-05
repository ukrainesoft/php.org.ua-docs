---
navigation:
  - function.ldap-delete-ext.md: « ldap\_delete\_ext
  - function.ldap-dn2ufn.md: ldap\_dn2ufn »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_delete
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_delete

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap\_delete — Видалення запису з директорії LDAP

### Опис

```methodsynopsis
ldap_delete(LDAP\Connection $ldap, string $dn, ?array $controls = null): bool
```

Видалення певного запису з директорії LDAP.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`dn`

Унікальне ім'я запису LDAP.

`controls`

Массив[керуючих констант LDAP](ldap.controls.md)для отправки в запросе.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.0.0 | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |
| 7.3.0 | Додано підтримку параметра `controls` |

### Дивіться також

-   [ldap\_delete\_ext()](function.ldap-delete-ext.md) \- Видалити запис із директорії
-   [ldap\_add()](function.ldap-add.md) \- Додати запис до LDAP директорії
