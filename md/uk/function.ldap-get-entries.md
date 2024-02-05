---
navigation:
  - function.ldap-get-dn.md: « ldap\_get\_dn
  - function.ldap-get-option.md: ldap\_get\_option »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_get\_entries
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_get\_entries

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap\_get\_entries — Отримує всі записи результату

### Опис

```methodsynopsis
ldap_get_entries(LDAP\Connection $ldap, LDAP\Result $result): array|false
```

Читає множинні записи із заданого результату, а потім читає атрибути та множинні значення.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`result`

Екземпляр [LDAP\\Result](class.ldap-result.md), що повертається [ldap\_list()](function.ldap-list.md) або [ldap\_search()](function.ldap-search.md)

### Значення, що повертаються

Повертає повну інформацію про результат у вигляді багатовимірного масиву у разі успішного виконання, та \*\*`false`\*\*в случае возникновения ошибки.

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

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [LDAP\\Result](class.ldap-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap result` |

### Дивіться також

-   [ldap\_first\_entry()](function.ldap-first-entry.md) \- Повернути перший ідентифікатор результату
-   [ldap\_next\_entry()](function.ldap-next-entry.md) \- Отримати наступний запис результату
