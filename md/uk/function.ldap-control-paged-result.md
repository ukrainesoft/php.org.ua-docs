- [« ldap_control_paged_result_response](function.ldap-control-paged-result-response.md)
- [ldap_count_entries »](function.ldap-count-entries.md)

- [PHP Manual](index.md)
- [Функції LDAP](ref.ldap.md)
- Надіслати серверу LDAP дані для використання посторінкового
отримання результату

#ldap_control_paged_result

(PHP 5 \>= 5.4.0, PHP 7)

ldap_control_paged_result — Надіслати серверу LDAP дані для
використання посторінкового отримання результату

**Увага**

Функція була оголошена *УСТАРНІЙ* у PHP 7.4.0 та *Видалена* у PHP 8.0.0.
Замість неї слід використовувати параметр `controls`
[ldap_search()](function.ldap-search.md). Дивіться також [Управляючі об'єкти LDAP](ldap.controls.md) для отримання додаткової
інформації.

### Опис

**ldap_control_paged_result**(
resource `$link`,
int `$pagesize`,
bool `$iscritical` = **`false`**,
string `$cookie` = ""
): bool

Дозволяє роботу з LDAP у посторінковому режимі, шляхом надсилання бажаних
налаштувань (розмір сторінки, куки тощо)

### Список параметрів

`link`
Ресурс LDAP, який повертається функцією
[ldap_connect()](function.ldap-connect.md).

`pagesize`
Кількість записів на сторінку.

`iscritical`
Визначає, чи є посторінковий режим критичним чи ні. Якщо
**`true`** і якщо сервер не підтримує посторінкову роботу, пошук
поверне порожній результат.

`cookie`
Непрозора структура, що надсилається сервером
([ldap_control_paged_result_response()](function.ldap-control-paged-result-response.md)).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Список змін

| Версія | Опис                          |
| ------ | ----------------------------- |
| 8.0.0  | Функцію було видалено.        |
| 7.4.0  | Функція оголошена застарілою. |

### Приклади

Приклад нижче демонструє вилучення першої сторінки результату пошуку з
використанням розміру сторінки, що дорівнює одному запису.

**Приклад #1 Посторінкова робота з LDAP**

`<?php     // $ds - ідентифікатор з'єднання (дивітьсяldap_connect)    ldap_set_option($ds, LDAP_OPT_PROTOCOL_VERSION, 3); $dn         = 'ou=example,dc=org'; $filter   = '(|(sn=Doe*)(givenname=John*))'; $justthese = array('ou', 'sn', 'givenname', 'mail'); // дозволяємо посторінкову роботу з розміром сторінки рівного одного запису. ldap_control_paged_result($ds, 1); $sr = ldap_search($ds, $dn, $filter, $justthese); $info = ldap_get_entries($ds, $sr); echo $info['count'] . ' записів повернено' . PHP_EOL; `

Приклад нижче демонструє вилучення першої сторінки результату пошуку з
використанням розміру сторінки дорівнює ста записам.

**Приклад #2 Посторінкова робота з LDAP**

`<?php     // $ds - ідентифікатор з'єднання(дивітьсяldap_connect)ldap_set_option($ds,LDAP_OPT_PROTOCOL_VERSION,3); $dn         = 'ou=example,dc=org'; $filter   = '(|(sn=Doe*)(givenname=John*))'; $justthese = array('ou', 'sn', 'givenname', 'mail'); // дозволяємо посторінкову роботу з розміром сторінки рівного ста записам. $pageSize = 100; $cookie==''; do {         ldap_control_paged_result($ds, $pageSize, true, $cookie); $result = ldap_search($ds, $dn, $filter, $justthese); $entries=ldap_get_entries($ds,$result); foreach ($entries as $e) {             echo $e['dn'] . PHP_EOL; }         ldap_control_paged_result_response($ds, $result, $cookie); } while($cookie !== null && $cookie != ''); `

### Примітки

> **Примітка**:
>
> Посторінковий режим з'явився у версії LDAPv3.

### Дивіться також

- [ldap_control_paged_result_response()](function.ldap-control-paged-result-response.md) -
Отримати вказівник на поточну сторінку результату LDAP
- [» RFC2696 : Модуль управління LDAP для простих маніпуляцій
постранично повертається результатом](http://www.faqs.org/rfcs/rfc2696)
