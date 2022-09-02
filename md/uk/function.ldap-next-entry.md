---
navigation:
  - function.ldap-next-attribute.md: « ldapnextattribute
  - function.ldap-next-reference.md: ldapnextreference »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapnextentry
---
# ldapnextentry

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapnextentry — Отримати наступний запис результату

### Опис

```methodsynopsis
ldap_next_entry(LDAP\Connection $ldap, LDAP\ResultEntry $entry): LDAP\ResultEntry|false
```

Отримати записи, які зберігаються в результаті. Наступні дзвінки **ldapnextentry()** повертають по одному запису, доки не залишиться більше записів. Перший виклик **ldapnextentry()** проводиться після виклику [ldapfirstentry()](function.ldap-first-entry.md) з параметром `entry`, який був повернутий [ldapfirstentry()](function.ldap-first-entry.md)

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.md), що повертається функцією [ldapconnect()](function.ldap-connect.md)

`entry`

Екземпляр [LDAPResultEntry](class.ldap-result-entry.md)

### Значення, що повертаються

Повертає екземпляр [LDAPResultEntry](class.ldap-result-entry.md) для наступного запису в результаті, вміст якого починають читатися, запускаючи [ldapfirstentry()](function.ldap-first-entry.md). Якщо немає більше записів у результаті, тоді повертається **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | Параметр `entry` тепер чекає екземпляр [LDAPResultEntry](class.ldap-result-entry.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | Повертає екземпляр [LDAPResult](class.ldap-result.md); раніше повертався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [ldapgetentries()](function.ldap-get-entries.md) - Отримує всі записи результату
