---
navigation:
  - function.ldap-delete-ext.md: « ldapdeleteext
  - function.ldap-dn2ufn.md: ldapdn2ufn »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapdelete
---
# ldapdelete

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapdelete — Видалення запису з директорії LDAP

### Опис

```methodsynopsis
ldap_delete(LDAP\Connection $ldap, string $dn, ?array $controls = null): bool
```

Видалення конкретного запису з директорії LDAP.

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.md), що повертається функцією [ldapconnect()](function.ldap-connect.md)

`dn`

Унікальне ім'я запису LDAP.

`controls`

Масив [управляющих констант LDAP](ldap.controls.md) для відправки у запиті.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |
|  | Додано підтримку параметра `controls` |

### Дивіться також

-   [ldapdeleteext()](function.ldap-delete-ext.md) - Видалити запис із директорії
-   [ldapadd()](function.ldap-add.md) - Додати запис до LDAP директорії
