---
navigation:
  - function.ldap-8859-to-t61.html: « ldapтоt61
  - function.ldap-add.html: ldapadd »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapaddext
---
# ldapaddext

(PHP 7> = 7.3.0, PHP 8)

ldapaddext — Додати записи до каталогу LDAP

### Опис

```methodsynopsis
ldap_add_ext(    LDAP\Connection $ldap,    string $dn,    array $entry,    ?array $controls = null): LDAP\Result|false
```

Робить те саме, що й [ldapadd()](function.ldap-add.html), але повертає екземпляр [LDAPResult](class.ldap-result.html) для розбору за допомогою [ldapparseresult()](function.ldap-parse-result.md)

### Список параметрів

Дивіться [ldapadd()](function.ldap-add.md)

### Значення, що повертаються

Повертає екземпляр [LDAPResult](class.ldap-result.md) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | Повертає екземпляр [LDAPResult](class.ldap-result.md); раніше повертався ресурс ([resource](language.types.resource.md) |
|  | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [ldapadd()](function.ldap-add.md) - Додати запис до LDAP директорії
-   [ldapparseresult()](function.ldap-parse-result.md) - Витягти інформацію з результату
