---
navigation:
  - function.ldap-first-attribute.md: « ldapfirstattribute
  - function.ldap-first-reference.md: ldapfirstreference »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapfirstentry
---
# ldapfirstentry

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapfirstentry — Повернути перший ідентифікатор результату

### Опис

```methodsynopsis
ldap_first_entry(LDAP\Connection $ldap, LDAP\Result $result): LDAP\ResultEntry|false
```

Повертає ідентифікатор першого запису в результаті. Цей ідентифікатор потім використовується у функції [ldapnextentry()](function.ldap-next-entry.md)для послідовного отримання записів з результату.

Записи в LDAP результаті зчитуються послідовно використовуючи функції **ldapfirstentry()** і [ldapnextentry()](function.ldap-next-entry.md)

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.md), що повертається функцією [ldapconnect()](function.ldap-connect.md)

`result`

Екземпляр [LDAPResult](class.ldap-result.md), що повертається [ldaplist()](function.ldap-list.md) або [ldapsearch()](function.ldap-search.md)

### Значення, що повертаються

Повертає екземпляр [LDAPResultEntry](class.ldap-result-entry.md) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | Параметр `result` тепер чекає екземпляр [LDAPResult](class.ldap-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | Повертає екземпляр [LDAPResultEntry](class.ldap-result-entry.md); раніше повертався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [ldapgetentries()](function.ldap-get-entries.md) - Отримує всі записи результату
