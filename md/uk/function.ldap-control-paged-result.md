---
navigation:
  - function.ldap-control-paged-result-response.md: « ldap\_control\_paged\_result\_response
  - function.ldap-count-entries.md: ldap\_count\_entries »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_control\_paged\_result
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_control\_paged\_result

(PHP 5 >= 5.4.0, PHP 7)

ldap\_control\_paged\_result — Надіслати серверу LDAP дані для використання посторінкового отримання результату

**Увага**

Функція була оголошена *застарілої* в PHP 7.4.0 та *ВИДАЛЕНО* у PHP 8.0.0. Замість неї слід використовувати параметр `controls`в[ldap\_search()](function.ldap-search.md)Смотрите также [Керуючі об'єкти LDAP](ldap.controls.md) для отримання додаткової інформації.

### Опис

```methodsynopsis
ldap_control_paged_result(    resource $link,    int $pagesize,    bool $iscritical = false,    string $cookie = ""): bool
```

Дозволяє працювати з LDAP у посторінковому режимі, шляхом надсилання бажаних налаштувань (розмір сторінки, куки і т.д.)

### Список параметрів

`link`

Ресурс LDAP, який повертається функцією [ldap\_connect()](function.ldap-connect.md)

`pagesize`

Кількість записів на сторінку.

`iscritical`

Визначає, чи є посторінковий режим критичним чи ні. Якщо **`true`** і якщо сервер не підтримує посторінкову роботу, пошук поверне порожній результат.

`cookie`

Непрозора структура, що посилається сервером ([ldap\_control\_paged\_result\_response()](function.ldap-control-paged-result-response.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функцію було видалено. |
| 7.4.0 | Функцію оголошено застарілою. |

### Приклади

Приклад нижче демонструє вилучення першої сторінки результату пошуку з використанням розміру сторінки, що дорівнює одному запису.

**Приклад #1 Посторінкова робота з LDAP**

```php
<?php
     // $ds - идентификатор соединения (смотрите ldap_connect)
     ldap_set_option($ds, LDAP_OPT_PROTOCOL_VERSION, 3);

     $dn        = 'ou=example,dc=org';
     $filter    = '(|(sn=Doe*)(givenname=John*))';
     $justthese = array('ou', 'sn', 'givenname', 'mail');

     // разрешаем постраничную работу с размером страницы равному одной записи.
     ldap_control_paged_result($ds, 1);

     $sr = ldap_search($ds, $dn, $filter, $justthese);

     $info = ldap_get_entries($ds, $sr);

     echo $info['count'] . ' записей возвращено' . PHP_EOL;
```

Приклад нижче демонструє вилучення першої сторінки результату пошуку з використанням розміру сторінки, що дорівнює ста записам.

**Приклад #2 Посторінкова робота з LDAP**

```php
<?php
     // $ds - идентификатор соединения (смотрите ldap_connect)
     ldap_set_option($ds, LDAP_OPT_PROTOCOL_VERSION, 3);

     $dn        = 'ou=example,dc=org';
     $filter    = '(|(sn=Doe*)(givenname=John*))';
     $justthese = array('ou', 'sn', 'givenname', 'mail');

     // разрешаем постраничную работу с размером страницы равному ста записям.
     $pageSize = 100;

     $cookie = '';
     do {
         ldap_control_paged_result($ds, $pageSize, true, $cookie);

         $result  = ldap_search($ds, $dn, $filter, $justthese);
         $entries = ldap_get_entries($ds, $result);

         foreach ($entries as $e) {
             echo $e['dn'] . PHP_EOL;
         }

         ldap_control_paged_result_response($ds, $result, $cookie);

     } while($cookie !== null && $cookie != '');
```

### Примітки

> **Зауваження** :
> 
> Посторовий режим з'явився у версії протоколу LDAPv3.

### Дивіться також

-   [ldap\_control\_paged\_result\_response()](function.ldap-control-paged-result-response.md) \- Отримати вказівник на поточну сторінку результуючого набору LDAP
-   [» RFC2696 : Керуючий модуль LDAP для простих маніпуляцій результатом, що посторінково повертається](http://www.faqs.org/rfcs/rfc2696)
