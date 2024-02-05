---
navigation:
  - function.ldap-control-paged-result.md: « ldap\_control\_paged\_result
  - function.ldap-count-references.md: ldap\_count\_references »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_count\_entries
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_count\_entries

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap\_count\_entries — Порахувати кількість записів у результатах пошуку

### Опис

```methodsynopsis
ldap_count_entries(LDAP\Connection $ldap, LDAP\Result $result): int
```

Повертає кількість записів, збережених у результаті попередньої операції пошуку.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`result`

Екземпляр [LDAP\\Result](class.ldap-result.md), що повертається [ldap\_list()](function.ldap-list.md) або [ldap\_search()](function.ldap-search.md)

### Значення, що повертаються

Повертає кількість записів у результаті або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [LDAP\\Result](class.ldap-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap result` |

### Приклади

**Пример #1 Пример использования функции**ldap\_count\_entries()\*\*\*\*

Отримання числа записів у результаті.

```php
// $ds допустимый экземпляр LDAP\Connection

     $dn        = 'ou=example,dc=org';
     $filter    = '(|(sn=Doe*)(givenname=John*))';
     $justthese = array('ou', 'sn', 'givenname', 'mail');

     $sr = ldap_search($ds, $dn, $filter, $justthese);

     var_dump(ldap_count_entries($ds, $sr));
```

Висновок наведеного прикладу буде схожим на:

```
int(1)
```
