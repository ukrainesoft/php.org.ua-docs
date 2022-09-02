---
navigation:
  - function.ldap-mod-del.md: « ldapmoddel
  - function.ldap-mod-replace.md: ldapmodreplace »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapmodreplaceext
---
# ldapmodreplaceext

(PHP 7> = 7.3.0, PHP 8)

ldapmodreplaceext — Замінити значення атрибута на нові

### Опис

```methodsynopsis
ldap_mod_replace_ext(    LDAP\Connection $ldap,    string $dn,    array $entry,    ?array $controls = null): LDAP\Result|false
```

Робить те саме, що й [ldapmodreplace()](function.ldap-mod-replace.md), але повертає екземпляр [LDAPResult](class.ldap-result.md) для розбору за допомогою [ldapparseresult()](function.ldap-parse-result.md)

### Список параметрів

Дивіться [ldapmodreplace()](function.ldap-mod-replace.md)

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

-   [ldapmodreplace()](function.ldap-mod-replace.md) - Замінити значення атрибутів на нові
-   [ldapparseresult()](function.ldap-parse-result.md) - Витягти інформацію з результату
