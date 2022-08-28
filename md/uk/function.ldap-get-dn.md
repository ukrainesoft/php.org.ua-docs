Отримати DN результуючого запису

-   [« ldap\_get\_attributes](function.ldap-get-attributes.html)
    
-   [ldap\_get\_entries »](function.ldap-get-entries.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LDAP](ref.ldap.html)
    
-   Отримати DN результуючого запису
    

# ldapgetдн

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapgetdn — Отримати DN результуючого запису

### Опис

```methodsynopsis
ldap_get_dn(LDAP\Connection $ldap, LDAP\ResultEntry $entry): string|false
```

Виявити DN запису в результаті.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.html), що повертається функцією [ldap\_connect()](function.ldap-connect.html)

`entry`

Екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.html)

### Значення, що повертаються

Повертає DN запису результату та **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                     |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html)     |
|        | Параметр `entry` тепер чекає екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.html); раніше очікувався ресурс ([resource](language.types.resource.html) |