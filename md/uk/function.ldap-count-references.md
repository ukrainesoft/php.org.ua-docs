Підраховує кількість посилань у результатах пошуку

-   [« ldap\_count\_entries](function.ldap-count-entries.html)
    
-   [ldap\_delete\_ext »](function.ldap-delete-ext.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LDAP](ref.ldap.html)
    
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

Екземпляр [LDAP\\Connection](class.ldap-connection.html), що повертається функцією [ldap\_connect()](function.ldap-connect.html)

`result`

Екземпляр [LDAP\\Result](class.ldap-result.html), що повертається [ldap\_list()](function.ldap-list.html) або [ldap\_search()](function.ldap-search.html)

### Значення, що повертаються

Повертає кількість посилань у результаті пошуку.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | Параметр `result` тепер чекає екземпляр [LDAP\\Result](class.ldap-result.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [ldap\_connect()](function.ldap-connect.html) - Підключитись до сервера LDAP