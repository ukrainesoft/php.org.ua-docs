Отримати вказівник на поточну сторінку LDAP

-   [« ldap\_connect](function.ldap-connect.html)
    
-   [ldap\_control\_paged\_result »](function.ldap-control-paged-result.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LDAP](ref.ldap.html)
    
-   Отримати вказівник на поточну сторінку LDAP
    

# ldapcontrolpagedresultresponse

(PHP 5> = 5.4.0, PHP 7)

ldapcontrolpagedresultresponse — Отримати вказівник на поточну сторінку LDAP

**Увага**

Функція була оголошена *застарілої* в PHP 7.4.0 та *ВИДАЛЕНО* у PHP 8.0.0. Замість неї слід використовувати параметр `controls` в [ldap\_search()](function.ldap-search.html). Дивіться також [Управляющие объекты LDAP](ldap.controls.html) для отримання додаткової інформації.

### Опис

```methodsynopsis
ldap_control_paged_result_response(    resource $link,    resource $result,    string &$cookie = ?,    int &$estimated = ?): bool
```

Отримати вказівник на поточну сторінку результуючого набору LDAP.

### Список параметрів

`link`

Ресурс LDAP, який повертається функцією [ldap\_connect()](function.ldap-connect.html)

`result`

`cookie`

Непрозора структура, отримана з сервера.

`estimated`

Очікувана кількість записів для вилучення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                      |
|--------|-------------------------------|
|        | Функцію було видалено.        |
|        | Функцію оголошено застарілою. |

### Дивіться також

-   [ldap\_control\_paged\_result()](function.ldap-control-paged-result.html) - Надіслати серверу LDAP дані для використання посторінкового отримання результату
-   [» RFC2696 : Управляющий модуль LDAP для простых манипуляций постранично возвращаемым результатом](http://www.faqs.org/rfcs/rfc2696)