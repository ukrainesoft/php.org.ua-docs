Повернути перший атрибут

-   [« ldapexplodeдн](function.ldap-explode-dn.html)
    
-   [ldapfirstentry »](function.ldap-first-entry.html)
    
-   [PHP Manual](index.html)
    
-   [Функції LDAP](ref.ldap.html)
    
-   Повернути перший атрибут
    

# ldapfirstattribute

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapfirstattribute — Повернути перший атрибут

### Опис

```methodsynopsis
ldap_first_attribute(LDAP\Connection $ldap, LDAP\ResultEntry $entry): string|false
```

Отримує перший атрибут у цьому записі. Атрибути, що залишаються, виходять послідовним викликом [ldapnextattribute()](function.ldap-next-attribute.html)

Подібно до читання записів, атрибути також читаються один за одним з окремого елемента.

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.html), що повертається функцією [ldapconnect()](function.ldap-connect.html)

`entry`

Екземпляр [LDAPResultEntry](class.ldap-result-entry.html)

`ber_identifier`

`ber_identifier` є ідентифікатором внутрішнього покажчика осередку пам'яті. Він передається за посиланням. Також `ber_identifier` передається в [ldapnextattribute()](function.ldap-next-attribute.html)яка змінює цей покажчик.

> **Зауваження**
> 
> Цей параметр більше не використовується, оскільки автоматично обробляється PHP. Для цілей зворотної сумісності, PHP не видає помилку, якщо цей параметр все ж таки передається.

### Значення, що повертаються

Повертає перший атрибут у записі, у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                   |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html)     |
|        | Параметр `entry` тепер чекає екземпляр [LDAPResultEntry](class.ldap-result-entry.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [ldapnextattribute()](function.ldap-next-attribute.html) - Отримати наступний атрибут із результату
-   [ldapgetattributes()](function.ldap-get-attributes.html) - Отримує атрибути із запису у результатах пошуку