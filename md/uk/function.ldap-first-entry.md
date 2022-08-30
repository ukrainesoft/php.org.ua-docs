Повернути перший ідентифікатор результату

-   [« ldapfirstattribute](function.ldap-first-attribute.html)
    
-   [ldapfirstreference »](function.ldap-first-reference.html)
    
-   [PHP Manual](index.html)
    
-   [Функції LDAP](ref.ldap.html)
    
-   Повернути перший ідентифікатор результату
    

# ldapfirstentry

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapfirstentry — Повернути перший ідентифікатор результату

### Опис

```methodsynopsis
ldap_first_entry(LDAP\Connection $ldap, LDAP\Result $result): LDAP\ResultEntry|false
```

Повертає ідентифікатор першого запису в результаті. Цей ідентифікатор потім використовується у функції [ldapnextentry()](function.ldap-next-entry.html)для послідовного отримання записів з результату.

Записи в LDAP результаті зчитуються послідовно використовуючи функції **ldapfirstentry()** і [ldapnextentry()](function.ldap-next-entry.html)

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.html), що повертається функцією [ldapconnect()](function.ldap-connect.html)

`result`

Екземпляр [LDAPResult](class.ldap-result.html), що повертається [ldaplist()](function.ldap-list.html) або [ldapsearch()](function.ldap-search.html)

### Значення, що повертаються

Повертає екземпляр [LDAPResultEntry](class.ldap-result-entry.html) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                               |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|        | Параметр `result` тепер чекає екземпляр [LDAPResult](class.ldap-result.html); раніше очікувався ресурс ([resource](language.types.resource.html)       |
|        | Повертає екземпляр [LDAPResultEntry](class.ldap-result-entry.html); раніше повертався ресурс ([resource](language.types.resource.html)                 |

### Дивіться також

-   [ldapgetentries()](function.ldap-get-entries.html) - Отримує всі записи результату