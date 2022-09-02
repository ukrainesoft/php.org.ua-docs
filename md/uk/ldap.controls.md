---
navigation:
  - ldap.using.md: « Використання дзвінків PHP LDAP
  - ldap.examples.md: Приклади »
  - index.md: PHP Manual
  - book.ldap.md: LDAP
title: Керуючі об'єкти LDAP
---
# Керуючі об'єкти LDAP

Керуючі об'єкти - це спеціальні об'єкти, які можуть бути передані спільно із запитом до LDAP для зміни його поведінки на час виконання запиту. Також це можуть бути об'єкти, що надсилаються сервером спільно з відповіддю на запит, зазвичай як відповіді на керуючі об'єкти, що прийшли з запитом, для надання додаткової інформації.

> **Зауваження**
> 
> Не всі об'єкти керування підтримуються всіма серверами LDAP. Щоб визначити, які з них підтримуються вашим сервером, виконайте запит кореневого DSE шляхом читання порожнього dn з фільтром (objectClass=
> 
> **Приклад #1 Тестування підтримки управління пагінацією результату**
> 
> ```php
> <?php
> 
> // $ds - корректный идентификатор соединения с сервером каталогов
> 
> $result = ldap_read($ds, '', '(objectClass=*)', ['supportedControl']);
> if (!in_array(LDAP_CONTROL_PAGEDRESULTS, ldap_get_entries($ds, $result)[0]['supportedcontrol'])) {
>   die("Этот сервер не поддерживает управление пагинацией");
> }
> 
> ?>
> ```

Починаючи з PHP 7.3, ви можете надсилати керуючі об'єкти паралельно із запитом для всіх функцій запитів, які приймають параметр serverctrls. Якщо існує "ext" версія функції, то для отримання повного доступу до всіх об'єктів відповіді та можливості розібрати відповідь за допомогою [ldapparseresult()](function.ldap-parse-result.md), Використовуйте саме її.

Параметр serverctrls повинен містити масив, що містить масив для кожного об'єкта, що посилається, з наступними ключами:

oid (string)

OID об'єкта, що управляє. Використовуйте константи LDAPCONTROL. Дивіться [константи LDAP](ldap.constants.md)

iscritical (bool)

Якщо об'єкт, що управляє, повинен бути позначений як критичний. Запит завершиться помилкою, якщо подібний керуючий об'єкт не підтримується сервером або якщо його неможливо застосувати. Зверніть увагу, що деякі об'єкти завжди повинні бути позначені як критичні, як описано у відповідному RFC. За замовчуванням **`false`**

value ([mixed](language.types.declarations.md#language.types.declarations.mixed)

Якщо застосовно, то значення об'єкта, що управляє. Докладніше читайте далі.

Більшість значень надсилаються на сервер закодованими BER. Ви можете займатися кодуванням самостійно, або використовувати масиви з коректними ключами, і тоді все відбудеться автоматично. Керовані об'єкти, що підтримуються:

-   **`LDAP_CONTROL_PAGEDRESULTS`** Очікувані ключі size і cookie
    
-   **`LDAP_CONTROL_ASSERT`** Очікуваний ключ - filter
    
-   **`LDAP_CONTROL_VALUESRETURNFILTER`** Очікуваний ключ - filter
    
-   **`LDAP_CONTROL_PRE_READ`** Очікуваний ключ - attrs
    
-   **`LDAP_CONTROL_POST_READ`** Очікуваний ключ - attrs
    
-   **`LDAP_CONTROL_SORTREQUEST`** Очікується масив масивів із ключами: attr, oid reverse
    
-   **`LDAP_CONTROL_VLVREQUEST`** Очікувані ключі: before, after, attrvalue | (offset, count), context
    

Для наступних об'єктів, що управляють, значення не потрібні:

-   **`LDAP_CONTROL_PASSWORDPOLICYREQUEST`**
    
-   **`LDAP_CONTROL_MANAGEDSAIT`**
    
-   **`LDAP_CONTROL_DONTUSECOPY`**
    

Об'єкт **`LDAP_CONTROL_PROXY_AUTHZ`** - Унікальний випадок, так як його значення не потрібно кодувати BER, так що ви можете використовувати звичайний рядок.

Якщо керуючі об'єкти передані у функцію [ldapparseresult()](function.ldap-parse-result.md), значення будуть перетворені на масив, якщо підтримуються. Підтримується таке:

-   **`LDAP_CONTROL_PASSWORDPOLICYRESPONSE`** Ключі: expire, grace, error
    
-   **`LDAP_CONTROL_PAGEDRESULTS`** Ключі: size, cookie
    
-   **`LDAP_CONTROL_PRE_READ`** Ключі: dn та імена атрибутів LDAP
    
-   **`LDAP_CONTROL_POST_READ`** Ключі: dn та імена атрибутів LDAP
    
-   **`LDAP_CONTROL_SORTRESPONSE`** Ключі: errcode, attribute
    
-   **`LDAP_CONTROL_VLVRESPONSE`** Ключі: target, count, errcode, context
