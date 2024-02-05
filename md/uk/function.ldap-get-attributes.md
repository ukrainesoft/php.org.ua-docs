---
navigation:
  - function.ldap-free-result.md: « ldap\_free\_result
  - function.ldap-get-dn.md: ldap\_get\_dn »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_get\_attributes
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_get\_attributes

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap\_get\_attributes — Отримує атрибути із запису в результатах пошуку

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

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`entry`

Екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.md)

### Значення, що повертаються

Повертає повну інформацію запису багатовимірний масив.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.1.0 | Параметр`entry` тепер чекає екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap result entry` |

### Приклади

**Приклад #1 Показує список атрибутів, які відповідають певному запису директорії**

```php
<?php
// $ds допустимый экземпляр LDAP\Connection

// $sr - действительный результат поиска из запроса
// к директории ldap

$entry = ldap_first_entry($ds, $sr);

$attrs = ldap_get_attributes($ds, $entry);

echo $attrs["count"] . " атрибуты, соответствующие этой записи:<p>";

for ($i=0; $i < $attrs["count"]; $i++) {
    echo $attrs[$i] . "<br />";
}
?>
```

### Дивіться також

-   [ldap\_first\_attribute()](function.ldap-first-attribute.md) \- Повернути перший атрибут
-   [ldap\_next\_attribute()](function.ldap-next-attribute.md) \- Отримати наступний атрибут із результату
