Сортує записи LDAP

-   [« ldapsetrebindproc](function.ldap-set-rebind-proc.html)
    
-   [ldapstarttls »](function.ldap-start-tls.html)
    
-   [PHP Manual](index.md)
    
-   [Функції LDAP](ref.ldap.md)
    
-   Сортує записи LDAP
    

# ldapsort

(PHP 4> = 4.2.0, PHP 5, PHP 7)

ldapsort — Сортування записів LDAP

**Увага**

Ця функція оголошена *застарілої*, починаючи з PHP 7.0.0 і була *ВИДАЛЕНО* у версії PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
ldap_sort(resource $link, resource $result, string $sortfilter): bool
```

Сортує результат запиту LDAP, який повертається функцією [ldapsearch()](function.ldap-search.html)

Так як ця функція сортує результат на стороні клієнта, ви можете отримати не ті результати, які очікували у випадку, якщо був перевищений ліміт `sizelimit` на стороні сервера або вказаний у [ldapsearch()](function.ldap-search.html)

### Список параметрів

`link`

Ресурс LDAP, який повертається функцією [ldapconnect()](function.ldap-connect.html)

`result`

Дескриптор результату пошуку, що повертається функцією [ldapsearch()](function.ldap-search.html)

`sortfilter`

Атрибут, що використовується як ключ при сортуванні.

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Описание               |
|--------|------------------------|
|        | Функцію було видалено. |

### Приклади

Сортування результатів пошуку.

**Приклад #1 Сортування LDAP**

```php
<?php
     // $ds - активный дескриптор соединения (смотрите ldap_connect)

     $dn        = 'ou=example,dc=org';
     $filter    = '(|(sn=Doe*)(givenname=John*))';
     $justthese = array('ou', 'sn', 'givenname', 'mail');

     $sr = ldap_search($ds, $dn, $filter, $justthese);

     // Сортировка
     ldap_sort($ds, $sr, 'sn');

     // Получение данных
     $info = ldap_get_entries($ds, $sr);
```