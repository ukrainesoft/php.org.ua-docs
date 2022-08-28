Надіслати серверу LDAP дані для використання посторінкового отримання результату

-   [« ldap\_control\_paged\_result\_response](function.ldap-control-paged-result-response.html)
    
-   [ldap\_count\_entries »](function.ldap-count-entries.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LDAP](ref.ldap.html)
    
-   Надіслати серверу LDAP дані для використання посторінкового отримання результату
    

# ldapcontrolpagedresult

(PHP 5> = 5.4.0, PHP 7)

ldapcontrolpagedresult — Надіслати серверу LDAP дані для використання посторінкового отримання результату

**Увага**

Функція була оголошена *Застарілої* в PHP 7.4.0 та *ВИДАЛЕНО* у PHP 8.0.0. Замість неї слід використовувати параметр `controls` в [ldap\_search()](function.ldap-search.html). Дивіться також [Управляющие объекты LDAP](ldap.controls.html) для отримання додаткової інформації.

### Опис

```methodsynopsis
ldap_control_paged_result(    resource $link,    int $pagesize,    bool $iscritical = false,    string $cookie = ""): bool
```

Дозволяє працювати з LDAP у посторінковому режимі, шляхом надсилання бажаних налаштувань (розмір сторінки, куки і т.д.)

### Список параметрів

`link`

Ресурс LDAP, який повертається функцією [ldap\_connect()](function.ldap-connect.html)

`pagesize`

Кількість записів на сторінку.

`iscritical`

Визначає, чи є посторінковий режим критичним чи ні. Якщо **`true`** і якщо сервер не підтримує посторінкову роботу, пошук поверне порожній результат.

`cookie`

Непрозора структура, що посилається сервером ([ldap\_control\_paged\_result\_response()](function.ldap-control-paged-result-response.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                      |
|--------|-------------------------------|
|        | Функцію було видалено.        |
|        | Функцію оголошено застарілою. |

### Приклади

Приклад нижче демонструє вилучення першої сторінки результату пошуку з використанням розміру сторінки, що дорівнює одному запису.

**Приклад #1 Посічна робота з LDAP**

```php
<?php
     // $ds - идентификатор соединения (смотрите ldap_connect)
     ldap_set_option($ds, LDAP_OPT_PROTOCOL_VERSION, 3);

     $dn        = 'ou=example,dc=org';
     $filter    = '(|(sn=Doe*)(givenname=John*))';
     $justthese = array('ou', 'sn', 'givenname', 'mail');

     // разрешаем постраничную работу с размером страницы равному одной записи.
     ldap_control_paged_result($ds, 1);

     $sr = ldap_search($ds, $dn, $filter, $justthese);

     $info = ldap_get_entries($ds, $sr);

     echo $info['count'] . ' записей возвращено' . PHP_EOL;
```

Приклад нижче демонструє вилучення першої сторінки результату пошуку з використанням розміру сторінки, що дорівнює ста записам.

**Приклад #2 Посторінкова робота з LDAP**

```php
<?php
     // $ds - идентификатор соединения (смотрите ldap_connect)
     ldap_set_option($ds, LDAP_OPT_PROTOCOL_VERSION, 3);

     $dn        = 'ou=example,dc=org';
     $filter    = '(|(sn=Doe*)(givenname=John*))';
     $justthese = array('ou', 'sn', 'givenname', 'mail');

     // разрешаем постраничную работу с размером страницы равному ста записям.
     $pageSize = 100;

     $cookie = '';
     do {
         ldap_control_paged_result($ds, $pageSize, true, $cookie);

         $result  = ldap_search($ds, $dn, $filter, $justthese);
         $entries = ldap_get_entries($ds, $result);

         foreach ($entries as $e) {
             echo $e['dn'] . PHP_EOL;
         }

         ldap_control_paged_result_response($ds, $result, $cookie);

     } while($cookie !== null && $cookie != '');
```

### Примітки

> **Зауваження**
> 
> Посторовий режим з'явився у версії протоколу LDAPv3.

### Дивіться також

-   [ldap\_control\_paged\_result\_response()](function.ldap-control-paged-result-response.html) - Отримати вказівник на поточну сторінку результуючого набору LDAP
-   [» RFC2696 : Управляющий модуль LDAP для простых манипуляций постранично возвращаемым результатом](http://www.faqs.org/rfcs/rfc2696)