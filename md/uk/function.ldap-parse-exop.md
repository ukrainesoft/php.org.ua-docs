Розбір результуючого об'єкта виконання розширеної операції LDAP

-   [« ldap\_next\_reference](function.ldap-next-reference.html)
    
-   [ldap\_parse\_reference »](function.ldap-parse-reference.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LDAP](ref.ldap.html)
    
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

Екземпляр [LDAP\\Connection](class.ldap-connection.html), що повертається функцією [ldap\_connect()](function.ldap-connect.html)

`result`

Екземпляр [LDAP\\Result](class.ldap-result.html), що повертається [ldap\_list()](function.ldap-list.html) або [ldap\_search()](function.ldap-search.html)

`response_data`

Буде заповнений розібраними даними.

`response_oid`

Буде заповнено поверненим OID.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | Параметр `result` тепер чекає екземпляр [LDAP\\Result](class.ldap-result.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [ldap\_exop()](function.ldap-exop.html) - Виконує розширену операцію