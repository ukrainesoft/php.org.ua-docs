---
navigation:
  - function.ldap-add.md: « ldapadd
  - function.ldap-bind.md: ldapbind »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapbindext
---
# ldapbindext

(PHP 7> = 7.3.0, PHP 8)

ldapbindext — Прив'язати до директорії LDAP

### Опис

```methodsynopsis
ldap_bind_ext(    LDAP\Connection $ldap,    ?string $dn = null,    ?string $password = null,    ?array $controls = null): LDAP\Result|false
```

Робить те саме, що й [ldapbind()](function.ldap-bind.md), але повертає екземпляр [LDAPResult](class.ldap-result.md) для розбору за допомогою [ldapparseresult()](function.ldap-parse-result.md)

### Список параметрів

Дивіться [ldapbind()](function.ldap-bind.md)

### Значення, що повертаються

Повертає екземпляр [LDAPResult](class.ldap-result.md) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | Повертає екземпляр [LDAPResult](class.ldap-result.md); раніше повертався ресурс ([resource](language.types.resource.md) |
|  | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |

### Дивіться також

-   [ldapbind()](function.ldap-bind.md) - Прив'язати до LDAP директорії
-   [ldapparseresult()](function.ldap-parse-result.md) - Витягти інформацію з результату
