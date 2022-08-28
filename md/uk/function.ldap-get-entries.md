Отримує всі записи результату

-   [« ldap\_get\_dn](function.ldap-get-dn.html)
    
-   [ldap\_get\_option »](function.ldap-get-option.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LDAP](ref.ldap.html)
    
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

Екземпляр [LDAP\\Connection](class.ldap-connection.html), що повертається функцією [ldap\_connect()](function.ldap-connect.html)

`result`

Екземпляр [LDAP\\Result](class.ldap-result.html), що повертається [ldap\_list()](function.ldap-list.html) або [ldap\_search()](function.ldap-search.html)

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

| Версия | Описание                                                                                                                                                 |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|        | Параметр `result` тепер чекає екземпляр [LDAP\\Result](class.ldap-result.html); раніше очікувався ресурс ([resource](language.types.resource.html)       |

### Дивіться також

-   [ldap\_first\_entry()](function.ldap-first-entry.html) - Повернути перший ідентифікатор результату
-   [ldap\_next\_entry()](function.ldap-next-entry.html) - Отримати наступний запис результату