Розірвати прив'язку до директорії LDAP

-   [« ldap\_t61\_to\_8859](function.ldap-t61-to-8859.html)
    
-   [LDAP\\Connection »](class.ldap-connection.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LDAP](ref.ldap.html)
    
-   Розірвати прив'язку до директорії LDAP
    

# ldapunbind

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapunbind — Розірвати прив'язку до директорії LDAP

### Опис

```methodsynopsis
ldap_unbind(LDAP\Connection $ldap): bool
```

Розриває прив'язку до LDAP-директорії.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.html), що повертається функцією [ldap\_connect()](function.ldap-connect.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                 |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [ldap\_bind()](function.ldap-bind.html) - Прив'язати до LDAP директорії