---
navigation:
  - function.ldap-connect.md: « ldap\_connect
  - function.ldap-control-paged-result.md: ldap\_control\_paged\_result »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_control\_paged\_result\_response
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_control\_paged\_result\_response

(PHP 5 >= 5.4.0, PHP 7)

ldap\_control\_paged\_result\_response — Отримати вказівник на поточну сторінку LDAP

**Увага**

Функція була оголошена *застарілої* в PHP 7.4.0 та *ВИДАЛЕНО* у PHP 8.0.0. Замість неї слід використовувати параметр `controls`в[ldap\_search()](function.ldap-search.md)Смотрите также [Керуючі об'єкти LDAP](ldap.controls.md) для отримання додаткової інформації.

### Опис

```methodsynopsis
ldap_control_paged_result_response(    resource $link,    resource $result,    string &$cookie = ?,    int &$estimated = ?): bool
```

Отримати вказівник поточної сторінки результуючого набору LDAP.

### Список параметрів

`link`

Ресурс LDAP, який повертається функцією [ldap\_connect()](function.ldap-connect.md)

`result`

`cookie`

Непрозора структура, отримана з сервера.

`estimated`

Очікувана кількість записів для вилучення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функцію було видалено. |
| 7.4.0 | Функцію оголошено застарілою. |

### Дивіться також

-   [ldap\_control\_paged\_result()](function.ldap-control-paged-result.md) \- Надіслати серверу LDAP дані для використання посторінкового отримання результату
-   [» RFC2696 : Керуючий модуль LDAP для простих маніпуляцій результатом, що посторінково повертається](http://www.faqs.org/rfcs/rfc2696)
