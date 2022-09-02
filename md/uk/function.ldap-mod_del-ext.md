---
navigation:
  - function.ldap-mod-add.md: « ldapmodadd
  - function.ldap-mod-del.md: ldapmoddel »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapmoddelext
---
# ldapmoddelext

(PHP 7> = 7.3.0, PHP 8)

ldapmoddelext — Видалити значення атрибутів із поточних атрибутів.

### Опис

```methodsynopsis
ldap_mod_del_ext(    LDAP\Connection $ldap,    string $dn,    array $entry,    ?array $controls = null): LDAP\Result|false
```

Робить те саме, що й [ldapmoddel()](function.ldap-mod-del.md), але повертає екземпляр [LDAPResult](class.ldap-result.md) для розбору за допомогою [ldapparseresult()](function.ldap-parse-result.md)

### Список параметрів

Дивіться [ldapmoddel()](function.ldap-mod-del.md)

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

-   [ldapmoddel()](function.ldap-mod-del.md) - Видалити значення атрибута із поточних атрибутів
-   [ldapparseresult()](function.ldap-parse-result.md) - Витягти інформацію з результату
