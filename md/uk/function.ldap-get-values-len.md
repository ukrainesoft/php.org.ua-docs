---
navigation:
  - function.ldap-get-option.html: « ldapgetoption
  - function.ldap-get-values.html: ldapgetvalues »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapgetvalueslen
---
# ldapgetvalueslen

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapgetvalueslen — Отримати всі бінарні значення із запису результату

### Опис

```methodsynopsis
ldap_get_values_len(LDAP\Connection $ldap, LDAP\ResultEntry $entry, string $attribute): array|false
```

Читає всі значення атрибута запису результату.

Ця функція використовується так само як і [ldapgetvalues()](function.ldap-get-values.md) за винятком того, що обробляє двійкові дані, а не рядкові.

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.html), що повертається функцією [ldapconnect()](function.ldap-connect.md)

`entry`

Екземпляр [LDAPResultEntry](class.ldap-result-entry.md)

`attribute`

### Значення, що повертаються

Повертає масив значень для атрибуту у разі успішного виконання та **`false`** у разі виникнення помилки. Окремі значення доступні за цілим індексом в масиві. Перший індекс 0. Число значень може бути знайдено за індексом "count" у результуючому масиві.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | Параметр `entry` тепер чекає екземпляр [LDAPResultEntry](class.ldap-result-entry.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [ldapgetvalues()](function.ldap-get-values.md) - Отримує всі значення із запису результату
