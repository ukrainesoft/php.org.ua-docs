Отримує всі записи результату

-   [« ldapgetдн](function.ldap-get-dn.html)
    
-   [ldapgetoption »](function.ldap-get-option.html)
    
-   [PHP Manual](index.html)
    
-   [Функції LDAP](ref.ldap.html)
    
-   Отримує всі записи результату
    

# ldapgetentries

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapgetentries — Отримує всі записи результату

### Опис

```methodsynopsis
ldap_get_entries(LDAP\Connection $ldap, LDAP\Result $result): array|false
```

Читає множинні записи із заданого результату, а потім читає атрибути та множинні значення.

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.html), що повертається функцією [ldapconnect()](function.ldap-connect.html)

`result`

Екземпляр [LDAPResult](class.ldap-result.html), що повертається [ldaplist()](function.ldap-list.html) або [ldapsearch()](function.ldap-search.html)

### Значення, що повертаються

Повертає повну інформацію про результат у вигляді багатовимірного масиву у разі успішного виконання, та **`false`** у разі виникнення помилки.

Структура масиву наступна: Індекс атрибута перетворено на нижній регістр. (Атрибути для серверів каталогів є нечутливими до регістру, але не тоді, коли вони використовуються як індекс масиву.)

```
return_value["count"] = число записей в результате
return_value[0] : ссылается на информацию о первой записи

return_value[i]["dn"] =  DN i-ой записи в результате

return_value[i]["count"] = число атрибутов в i-ой записи
return_value[i][j] = NAME j-ого атрибута в i-ой записи результата

return_value[i]["attribute"]["count"] = число значений атрибута в
                                        i-ой записи
return_value[i]["attribute"][j] = j-ое значение атрибута i-ой записи
```

### список змін

| Версия | Описание                                                                                                                                               |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|        | Параметр `result` тепер чекає екземпляр [LDAPResult](class.ldap-result.html); раніше очікувався ресурс ([resource](language.types.resource.html)       |

### Дивіться також

-   [ldapfirstentry()](function.ldap-first-entry.html) - Повернути перший ідентифікатор результату
-   [ldapnextentry()](function.ldap-next-entry.html) - Отримати наступний запис результату