---
navigation:
  - function.ldap-next-attribute.md: « ldap\_next\_attribute
  - function.ldap-next-reference.md: ldap\_next\_reference »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_next\_entry
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_next\_entry

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap\_next\_entry — Отримати наступний запис результату

### Опис

```methodsynopsis
ldap_next_entry(LDAP\Connection $ldap, LDAP\ResultEntry $entry): LDAP\ResultEntry|false
```

Отримати записи, які зберігаються в результаті. Наступні дзвінки **ldap\_next\_entry()** повертають по одному запису, доки не залишиться більше записів. Перший виклик **ldap\_next\_entry()** проводиться після виклику [ldap\_first\_entry()](function.ldap-first-entry.md)с параметром`entry`, який був повернутий [ldap\_first\_entry()](function.ldap-first-entry.md)

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`entry`

Екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.md)

### Значення, що повертаються

Повертає екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.md) для наступного запису в результаті, вміст якого починають читатися, запускаючи [ldap\_first\_entry()](function.ldap-first-entry.md). Якщо немає більше записів у результаті, тоді повертається **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.1.0 | Параметр`entry` тепер чекає екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap result entry` |
| 8.1.0 | Повертає екземпляр [LDAP\\Result](class.ldap-result.md); раніше повертався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [ldap\_get\_entries()](function.ldap-get-entries.md) \- Отримує всі записи результату
