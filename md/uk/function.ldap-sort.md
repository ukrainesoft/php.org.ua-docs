---
navigation:
  - function.ldap-set-rebind-proc.md: « ldap\_set\_rebind\_proc
  - function.ldap-start-tls.md: ldap\_start\_tls »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_sort
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_sort

(PHP 4 >= 4.2.0, PHP 5, PHP 7)

ldap\_sort — Сортування записів LDAP

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.0.0 і була *ВИДАЛЕНО* у версії PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
ldap_sort(resource $link, resource $result, string $sortfilter): bool
```

Сортує результат запиту LDAP, який повертається функцією [ldap\_search()](function.ldap-search.md)

Так як ця функція сортує результат на клієнтській стороні, ви можете отримати не ті результати, які очікували, якщо був перевищений ліміт `sizelimit` на стороні сервера або вказаний у [ldap\_search()](function.ldap-search.md)

### Список параметрів

`link`

Ресурс LDAP, який повертається функцією [ldap\_connect()](function.ldap-connect.md)

`result`

Дескриптор результату пошуку, що повертається функцією [ldap\_search()](function.ldap-search.md)

`sortfilter`

Атрибут, що використовується як ключ при сортуванні.

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функцію було видалено. |

### Приклади

Сортування результатів пошуку.

**Приклад #1 Сортування LDAP**

```php
<?php
     // $ds - активный дескриптор соединения (смотрите ldap_connect)

     $dn        = 'ou=example,dc=org';
     $filter    = '(|(sn=Doe*)(givenname=John*))';
     $justthese = array('ou', 'sn', 'givenname', 'mail');

     $sr = ldap_search($ds, $dn, $filter, $justthese);

     // Сортировка
     ldap_sort($ds, $sr, 'sn');

     // Получение данных
     $info = ldap_get_entries($ds, $sr);
```
