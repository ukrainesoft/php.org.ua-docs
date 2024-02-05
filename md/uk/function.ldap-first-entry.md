---
navigation:
  - function.ldap-first-attribute.md: « ldap\_first\_attribute
  - function.ldap-first-reference.md: ldap\_first\_reference »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_first\_entry
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_first\_entry

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap\_first\_entry — Повернути перший ідентифікатор результату

### Опис

```methodsynopsis
ldap_first_entry(LDAP\Connection $ldap, LDAP\Result $result): LDAP\ResultEntry|false
```

Повертає ідентифікатор першого запису в результаті. Цей ідентифікатор потім використовується у функції [ldap\_next\_entry()](function.ldap-next-entry.md)для послідовного отримання записів з результату.

Записи в LDAP результаті зчитуються послідовно використовуючи функції \*\*ldap\_first\_entry()\*\*и[ldap\_next\_entry()](function.ldap-next-entry.md)

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`result`

Екземпляр [LDAP\\Result](class.ldap-result.md), що повертається [ldap\_list()](function.ldap-list.md) або [ldap\_search()](function.ldap-search.md)

### Значення, що повертаються

Повертає екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.md)или\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [LDAP\\Result](class.ldap-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap result` |
| 8.1.0 | Повертає екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.md); раніше повертався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [ldap\_get\_entries()](function.ldap-get-entries.md) \- Отримує всі записи результату
