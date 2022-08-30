Підраховує кількість посилань у результатах пошуку

-   [« ldapcountentries](function.ldap-count-entries.html)
    
-   [ldapdeleteext »](function.ldap-delete-ext.html)
    
-   [PHP Manual](index.html)
    
-   [Функції LDAP](ref.ldap.html)
    
-   Підраховує кількість посилань у результатах пошуку
    

# ldapcountreferences

(PHP 8)

ldapcountreferences — Підраховує кількість посилань у результатах пошуку

### Опис

```methodsynopsis
ldap_count_references(LDAP\Connection $ldap, LDAP\Result $result): int
```

Підраховує кількість посилань у результатах пошуку.

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.html), що повертається функцією [ldapconnect()](function.ldap-connect.html)

`result`

Екземпляр [LDAPResult](class.ldap-result.html), що повертається [ldaplist()](function.ldap-list.html) або [ldapsearch()](function.ldap-search.html)

### Значення, що повертаються

Повертає кількість посилань у результаті пошуку.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | Параметр `result` тепер чекає екземпляр [LDAPResult](class.ldap-result.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [ldapconnect()](function.ldap-connect.html) - Підключитись до сервера LDAP