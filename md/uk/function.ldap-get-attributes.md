---
navigation:
  - function.ldap-free-result.md: « ldapfreeresult
  - function.ldap-get-dn.md: ldapgetdn »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapgetattributes
---
# ldapgetattributes

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapgetattributes — Отримує атрибути із запису в результатах пошуку

### Опис

```methodsynopsis
ldap_get_attributes(LDAP\Connection $ldap, LDAP\ResultEntry $entry): array
```

Читає атрибути та значення із запису у результатах пошуку.

Визначивши розташування певного запису в каталозі, ви можете дізнатися, яка інформація зберігається для цього запису, використовуючи цю функцію. Ви повинні використовувати цю функцію для програми, яка "переглядає" записи каталогу та/або де структура записів каталогу невідома. У багатьох програмах ви шукатимете певний атрибут, такий як адреса електронної пошти або прізвище, не торкаючись інших даних.

```
return_value["count"] = число атрибутов в записи
return_value[0] = первый атрибут
return_value[n] = n-ый атрибут

return_value["attribute"]["count"] = число значений атрибута
return_value["attribute"][0] = первое значение атрибута
return_value["attribute"][i] = (i+1)-ое значение атрибута
```

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.md), що повертається функцією [ldapconnect()](function.ldap-connect.md)

`entry`

Екземпляр [LDAPResultEntry](class.ldap-result-entry.md)

### Значення, що повертаються

Повертає повну інформацію запису в багатовимірний масив у разі успішного виконання та **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | Параметр `entry` тепер чекає екземпляр [LDAPResultEntry](class.ldap-result-entry.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Показує список атрибутів, які відповідають певному запису директорії**

```php
<?php
// $ds допустимый экземпляр LDAP\Connection

// $sr - действительный результат поиска из запроса
// к директории ldap

$entry = ldap_first_entry($ds, $sr);

$attrs = ldap_get_attributes($ds, $entry);

echo $attrs["count"] . " атрибуты, соответствующие этой записи:<p>";

for ($i=0; $i < $attrs["count"]; $i++) {
    echo $attrs[$i] . "<br />";
}
?>
```

### Дивіться також

-   [ldapfirstattribute()](function.ldap-first-attribute.md) - Повернути перший атрибут
-   [ldapnextattribute()](function.ldap-next-attribute.md) - Отримати наступний атрибут із результату
