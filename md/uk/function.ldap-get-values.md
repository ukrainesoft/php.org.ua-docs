Отримує всі значення із запису результату

-   [« ldapgetvalueslen](function.ldap-get-values-len.html)
    
-   [ldaplist »](function.ldap-list.html)
    
-   [PHP Manual](index.md)
    
-   [Функції LDAP](ref.ldap.md)
    
-   Отримує всі значення із запису результату
    

# ldapgetvalues

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapgetvalues ​​— Отримує всі значення із запису результату

### Опис

```methodsynopsis
ldap_get_values(LDAP\Connection $ldap, LDAP\ResultEntry $entry, string $attribute): array|false
```

Читає всі значення атрибута запису результату.

Ця функція вимагає `entry`, а отже, перед нею повинні бути запущені одна з функцій пошуку ldap і один з результатів їх виклику для отримання окремого запису.

У додатку необхідно буде використовувати складні конструкції для пошуку певних атрибутів (таких як "прізвище" або "пошта") або необхідно буде використовувати функцію [ldapgetattributes()](function.ldap-get-attributes.html), щоб розібрати, які атрибути існують для запису.

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.html), що повертається функцією [ldapconnect()](function.ldap-connect.html)

`entry`

Екземпляр [LDAPResultEntry](class.ldap-result-entry.html)

`attribute`

### Значення, що повертаються

Повертає масив значень для атрибуту у разі успішного виконання або **`false`** у разі виникнення помилки. Число значень може бути знайдено за індексом "count" у результуючому масиві. Окремі значення можуть бути доступні за цілими індексами в масиві. Перший індекс 0.

LDAP дозволяє зберігати більше одного запису для атрибута, таким чином, можна, наприклад, зберегти багато адрес електронної пошти для запису каталогу однієї людини, всі марковані атрибутом "mail"

```
 return\_value\["count"\] = число значений атрибута
 return\_value\[0\] = первое значение атрибута
 return\_value\[i\] = i-ое значение атрибута 
```

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | Параметр `entry` тепер чекає екземпляр [LDAPResultEntry](class.ldap-result-entry.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Список усіх значень атрибуту "mail" для запису каталогу**

```php
<?php
// $ds допустимый экземпляр LDAP\Connection

// $sr верный результат поиска в директории ldap

// $entry верный идентификатор записи из вызова функции
//        вернувшей запись директории

$values = ldap_get_values($ds, $entry, "mail");

echo $values["count"] . " адреса email для этой записи.<br />";

for ($i=0; $i < $values["count"]; $i++) {
    echo $values[$i] . "<br />";
}
?>
```

### Дивіться також

-   [ldapgetvalueslen()](function.ldap-get-values-len.html) - Отримати всі бінарні значення із запису результату