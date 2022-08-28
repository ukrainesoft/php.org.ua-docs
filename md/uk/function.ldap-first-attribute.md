Повернути перший атрибут

-   [« ldap\_explode\_dn](function.ldap-explode-dn.html)
    
-   [ldap\_first\_entry »](function.ldap-first-entry.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LDAP](ref.ldap.html)
    
-   Повернути перший атрибут
    

# ldapfirstattribute

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapfirstattribute — Повернути перший атрибут

### Опис

```methodsynopsis
ldap_first_attribute(LDAP\Connection $ldap, LDAP\ResultEntry $entry): string|false
```

Отримує перший атрибут у цьому записі. Атрибути, що залишаються, виходять послідовним викликом [ldap\_next\_attribute()](function.ldap-next-attribute.html)

Подібно до читання записів, атрибути також читаються один за одним з окремого елемента.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.html), що повертається функцією [ldap\_connect()](function.ldap-connect.html)

`entry`

Екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.html)

`ber_identifier`

`ber_identifier` є ідентифікатором внутрішнього покажчика осередку пам'яті. Він передається за посиланням. Також `ber_identifier` передається в [ldap\_next\_attribute()](function.ldap-next-attribute.html)яка змінює цей покажчик.

> **Зауваження**
> 
> Цей параметр більше не використовується, оскільки автоматично обробляється PHP. Для цілей зворотної сумісності, PHP не видає помилку, якщо цей параметр все ж таки передається.

### Значення, що повертаються

Повертає перший атрибут у записі, у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                     |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html)     |
|        | Параметр `entry` тепер чекає екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [ldap\_next\_attribute()](function.ldap-next-attribute.html) - Отримати наступний атрибут із результату
-   [ldap\_get\_attributes()](function.ldap-get-attributes.html) - Отримує атрибути із запису у результатах пошуку