---
navigation:
  - function.ldap-control-paged-result.html: « ldapcontrolpagedresult
  - function.ldap-count-references.html: ldapcountreferences »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapcountentries
---
# ldapcountentries

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapcountentries — Порахувати кількість записів у результатах пошуку

### Опис

```methodsynopsis
ldap_count_entries(LDAP\Connection $ldap, LDAP\Result $result): int
```

Повертає кількість записів, збережених у результаті попередньої операції пошуку.

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.html), що повертається функцією [ldapconnect()](function.ldap-connect.md)

`result`

Екземпляр [LDAPResult](class.ldap-result.html), що повертається [ldaplist()](function.ldap-list.html) або [ldapsearch()](function.ldap-search.md)

### Значення, що повертаються

Повертає кількість записів у результаті або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | Параметр `result` тепер чекає екземпляр [LDAPResult](class.ldap-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання функції **ldapcountentries()****

Отримання числа записів у результаті.

```php
// $ds допустимый экземпляр LDAP\Connection

     $dn        = 'ou=example,dc=org';
     $filter    = '(|(sn=Doe*)(givenname=John*))';
     $justthese = array('ou', 'sn', 'givenname', 'mail');

     $sr = ldap_search($ds, $dn, $filter, $justthese);

     var_dump(ldap_count_entries($ds, $sr));
```

Результатом виконання цього прикладу буде щось подібне:

```
int(1)
```
