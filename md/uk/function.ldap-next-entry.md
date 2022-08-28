Отримати наступний запис результату

-   [« ldap\_next\_attribute](function.ldap-next-attribute.html)
    
-   [ldap\_next\_reference »](function.ldap-next-reference.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LDAP](ref.ldap.html)
    
-   Отримати наступний запис результату
    

# ldapnextentry

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapnextentry — Отримати наступний запис результату

### Опис

```methodsynopsis
ldap_next_entry(LDAP\Connection $ldap, LDAP\ResultEntry $entry): LDAP\ResultEntry|false
```

Отримати записи, які зберігаються в результаті. Наступні дзвінки **ldapnextentry()** повертають по одному запису, доки не залишиться більше записів. Перший виклик **ldapnextentry()** проводиться після виклику [ldap\_first\_entry()](function.ldap-first-entry.html) з параметром `entry`, який був повернутий [ldap\_first\_entry()](function.ldap-first-entry.html)

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.html), що повертається функцією [ldap\_connect()](function.ldap-connect.html)

`entry`

Екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.html)

### Значення, що повертаються

Повертає екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.html) для наступного запису в результаті, вміст якого починають читатися, запускаючи [ldap\_first\_entry()](function.ldap-first-entry.html). Якщо немає більше записів у результаті, тоді повертається **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | Параметр `entry` тепер чекає екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | Повертає екземпляр [LDAP\\Result](class.ldap-result.html); раніше повертався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [ldap\_get\_entries()](function.ldap-get-entries.html) - Отримує всі записи результату