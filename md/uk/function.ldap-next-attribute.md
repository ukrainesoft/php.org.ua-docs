---
navigation:
  - function.ldap-modify.html: « ldapmodify
  - function.ldap-next-entry.html: ldapnextentry »
  - index.html: PHP Manual
  - ref.ldap.html: Функції LDAP
title: ldapnextattribute
---
# ldapnextattribute

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapnextattribute — Отримати наступний атрибут із результату

### Опис

```methodsynopsis
ldap_next_attribute(LDAP\Connection $ldap, LDAP\ResultEntry $entry): string|false
```

Повертає атрибути запису. Перший виклик **ldapnextattribute()** проводиться з параметром `entry`, який повертається [ldapfirstattribute()](function.ldap-first-attribute.md)

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.html), що повертається функцією [ldapconnect()](function.ldap-connect.md)

`entry`

Екземпляр [LDAPResultEntry](class.ldap-result-entry.md)

`ber_identifier`

Внутрішній стан вказівника зберігається цим параметром.

> **Зауваження**
> 
> Параметр більше не використовується, оскільки це автоматично обробляється PHP. Для зворотної сумісності PHP не буде викидати помилку, якщо цей параметр буде передано.

### Значення, що повертаються

Повертає наступний атрибут запису у разі успішного виконання та **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | Параметр `entry` тепер чекає екземпляр [LDAPResultEntry](class.ldap-result-entry.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [ldapgetattributes()](function.ldap-get-attributes.md) - Отримує атрибути із запису у результатах пошуку
