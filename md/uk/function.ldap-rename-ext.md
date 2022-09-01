---
navigation:
  - function.ldap-read.html: « ldapread
  - function.ldap-rename.html: ldaprename »
  - index.html: PHP Manual
  - ref.ldap.html: Функції LDAP
title: ldaprenameext
---
# ldaprenameext

(PHP 7> = 7.3.0, PHP 8)

ldaprenameext — Модифікувати назву запису

### Опис

```methodsynopsis
ldap_rename_ext(    LDAP\Connection $ldap,    string $dn,    string $new_rdn,    string $new_parent,    bool $delete_old_rdn,    ?array $controls = null): LDAP\Result|false
```

Робить те саме, що й [ldaprename()](function.ldap-rename.html), але повертає екземпляр [LDAPResult](class.ldap-result.html) для розбору за допомогою [ldapparseresult()](function.ldap-parse-result.html)

### Список параметрів

Дивіться [ldaprename()](function.ldap-rename.html)

### Значення, що повертаються

Повертає екземпляр [LDAPResult](class.ldap-result.html) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | Повертає екземпляр [LDAPResult](class.ldap-result.html); раніше повертався ресурс ([resource](language.types.resource.html) |
|  | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |
|  | Додано підтримку параметра `controls` |

### Дивіться також

-   [ldaprename()](function.ldap-rename.html) - Змінити ім'я запису
-   [ldapparseresult()](function.ldap-parse-result.html) - Витягти інформацію з результату
