Обертка для розширеної операції WHOAMI

-   [« ldapexoprefresh](function.ldap-exop-refresh.html)
    
-   [ldapexop »](function.ldap-exop.html)
    
-   [PHP Manual](index.html)
    
-   [Функції LDAP](ref.ldap.html)
    
-   Обертка для розширеної операції WHOAMI
    

# ldapexopwhoami

(PHP 7> = 7.2.0, PHP 8)

ldapexopwhoami — Обертка для розширеної операції WHOAMI

### Опис

```methodsynopsis
ldap_exop_whoami(LDAP\Connection $ldap): string|false
```

Виконує розширену операцію WHOAMI та повертає дані.

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.html), що повертається функцією [ldapconnect()](function.ldap-connect.html)

### Значення, що повертаються

Дані, повернуті сервером, або **`false`**

### список змін

| Версия | Описание                                                                                                                                               |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [ldapexop()](function.ldap-exop.html) - Виконує розширену операцію