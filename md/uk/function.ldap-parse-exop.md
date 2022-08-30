Розбір результуючого об'єкта виконання розширеної операції LDAP

-   [« ldapnextreference](function.ldap-next-reference.html)
    
-   [ldapparsereference »](function.ldap-parse-reference.html)
    
-   [PHP Manual](index.md)
    
-   [Функції LDAP](ref.ldap.md)
    
-   Розбір результуючого об'єкта виконання розширеної операції LDAP
    

# ldapparseexop

(PHP 7> = 7.2.0, PHP 8)

ldapparseexop — Розбір результуючого об'єкта виконання розширеної операції LDAP

### Опис

```methodsynopsis
ldap_parse_exop(    LDAP\Connection $ldap,    LDAP\Result $result,    string &$response_data = null,    string &$response_oid = null): bool
```

Розбирає `result`отриманий після виконання розширеної операції LDAP

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.html), що повертається функцією [ldapconnect()](function.ldap-connect.html)

`result`

Екземпляр [LDAPResult](class.ldap-result.html), що повертається [ldaplist()](function.ldap-list.html) або [ldapsearch()](function.ldap-search.html)

`response_data`

Буде заповнений розібраними даними.

`response_oid`

Буде заповнено поверненим OID.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | Параметр `result` тепер чекає екземпляр [LDAPResult](class.ldap-result.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [ldapexop()](function.ldap-exop.html) - Виконує розширену операцію