---
navigation:
  - function.ldap-get-values-len.md: « ldap\_get\_values\_len
  - function.ldap-list.md: ldap\_list »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_get\_values
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_get\_values

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap\_get\_values ​​— Отримує всі значення із запису результату

### Опис

```methodsynopsis
ldap_get_values(LDAP\Connection $ldap, LDAP\ResultEntry $entry, string $attribute): array|false
```

Читає всі значення атрибута запису результату.

Ця функція вимагає `entry`, а отже, перед нею повинна бути запущена одна з функцій пошуку ldap і один з результатів їх виклику для отримання окремого запису.

У додатку необхідно буде використовувати складні конструкції для пошуку певних атрибутів (таких як "прізвище" або "пошта") або необхідно буде використовувати функцію [ldap\_get\_attributes()](function.ldap-get-attributes.md), щоб розібрати, які атрибути існують для запису.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`entry`

Екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.md)

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

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.1.0 | Параметр`entry` тепер чекає екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap result entry` |

### Приклади

**Приклад #1 Список усіх значень атрибуту "mail" для запису каталогу**

```php
<?php
// $ds допустимый экземпляр LDAP\Connection

// $sr верный результат поиска в директории ldap

// $entry верный идентификатор записи из вызова функции
//        вернувшей запись директории

$values = ldap_get_values($ds, $entry, "mail");

echo $values["count"] . " адреса email для этой записи.<br />";

for ($i=0; $i < $values["count"]; $i++) {
    echo $values[$i] . "<br />";
}
?>
```

### Дивіться також

-   [ldap\_get\_values\_len()](function.ldap-get-values-len.md) \- Отримати всі бінарні значення із запису результату
