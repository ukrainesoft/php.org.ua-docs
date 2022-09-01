---
navigation:
  - function.ldap-list.html: « ldaplist
  - function.ldap-mod-add.html: ldapmodadd »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapmodaddext
---
# ldapmodaddext

(PHP 7> = 7.3.0, PHP 8)

ldapmodaddext — Додати значення атрибуту до поточних атрибутів

### Опис

```methodsynopsis
ldap_mod_add_ext(    LDAP\Connection $ldap,    string $dn,    array $entry,    ?array $controls = null): LDAP\Result|false
```

Робить те саме, що й [ldapmodadd()](function.ldap-mod-add.html), але повертає екземпляр [LDAPResult](class.ldap-result.html) для розбору за допомогою [ldapparseresult()](function.ldap-parse-result.html)

### Список параметрів

Дивіться [ldapmodadd()](function.ldap-mod-add.html)

### Значення, що повертаються

Повертає екземпляр [LDAPResult](class.ldap-result.html) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | Повертає екземпляр [LDAPResult](class.ldap-result.html); раніше повертався ресурс ([resource](language.types.resource.md) |
|  | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |
|  | Додано підтримку параметра `controls` |

### Дивіться також

-   [ldapmodadd()](function.ldap-mod-add.html) - Додати значення атрибуту до поточних атрибутів
-   [ldapparseresult()](function.ldap-parse-result.html) - Витягти інформацію з результату
