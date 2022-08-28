Повернути перший ідентифікатор результату

-   [« ldap\_first\_attribute](function.ldap-first-attribute.html)
    
-   [ldap\_first\_reference »](function.ldap-first-reference.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LDAP](ref.ldap.html)
    
-   Повернути перший ідентифікатор результату
    

# ldapfirstentry

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapfirstentry — Повернути перший ідентифікатор результату

### Опис

```methodsynopsis
ldap_first_entry(LDAP\Connection $ldap, LDAP\Result $result): LDAP\ResultEntry|false
```

Повертає ідентифікатор першого запису в результаті. Цей ідентифікатор потім використовується у функції [ldap\_next\_entry()](function.ldap-next-entry.html)для послідовного отримання записів з результату.

Записи в LDAP результаті зчитуються послідовно використовуючи функції **ldapfirstentry()** і [ldap\_next\_entry()](function.ldap-next-entry.html)

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.html), що повертається функцією [ldap\_connect()](function.ldap-connect.html)

`result`

Екземпляр [LDAP\\Result](class.ldap-result.html), що повертається [ldap\_list()](function.ldap-list.html) або [ldap\_search()](function.ldap-search.html)

### Значення, що повертаються

Повертає екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.html) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                 |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|        | Параметр `result` тепер чекає екземпляр [LDAP\\Result](class.ldap-result.html); раніше очікувався ресурс ([resource](language.types.resource.html)       |
|        | Повертає екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.html); раніше повертався ресурс ([resource](language.types.resource.html)                 |

### Дивіться також

-   [ldap\_get\_entries()](function.ldap-get-entries.html) - Отримує всі записи результату