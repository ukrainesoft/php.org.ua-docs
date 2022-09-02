---
navigation:
  - function.ldap-read.md: « ldapread
  - function.ldap-rename.md: ldaprename »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldaprenameext
---
# ldaprenameext

(PHP 7> = 7.3.0, PHP 8)

ldaprenameext — Модифікувати назву запису

### Опис

```methodsynopsis
ldap_rename_ext(    LDAP\Connection $ldap,    string $dn,    string $new_rdn,    string $new_parent,    bool $delete_old_rdn,    ?array $controls = null): LDAP\Result|false
```

Робить те саме, що й [ldaprename()](function.ldap-rename.md), але повертає екземпляр [LDAPResult](class.ldap-result.md) для розбору за допомогою [ldapparseresult()](function.ldap-parse-result.md)

### Список параметрів

Дивіться [ldaprename()](function.ldap-rename.md)

### Значення, що повертаються

Повертає екземпляр [LDAPResult](class.ldap-result.md) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | Повертає екземпляр [LDAPResult](class.ldap-result.md); раніше повертався ресурс ([resource](language.types.resource.md) |
|  | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |
|  | Додано підтримку параметра `controls` |

### Дивіться також

-   [ldaprename()](function.ldap-rename.md) - Змінити ім'я запису
-   [ldapparseresult()](function.ldap-parse-result.md) - Витягти інформацію з результату
