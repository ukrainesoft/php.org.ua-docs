---
navigation:
  - function.yaz-es-result.md: « yaz\_es\_result
  - function.yaz-get-option.md: yaz\_get\_option »
  - index.md: PHP Manual
  - ref.yaz.md: Функції YAZ
title: yaz\_es
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# yaz\_es

(PECL yaz >= 0.9.0)

yaz\_es — готує Extended Service Request

### Опис

```methodsynopsis
yaz_es(
    resource $id
   , 
    string $type
   , 
    array $args
   ): void
```

Функція готує Extended Service Request. Extended Services – це сімейство різних засобів Z39.50, таких як оновлення записів, порядок елементів, адміністрування баз даних тощо.

> **Зауваження** :
> 
> Чимало серверів Z39.50 не підтримують Extended Services.

**yaz\_es()** створює пакети Extended Service Request і поміщає в чергу операцій. Використовуйте [yaz\_wait()](function.yaz-wait.md)для отправки запроса(ов) на сервер. После завершения[yaz\_wait()](function.yaz-wait.md), результату операцій Extended Service слід очікувати за допомогою дзвінка [yaz\_es\_result()](function.yaz-es-result.md)

### Список параметрів

`id`

Ресурс підключення, що повертається [yaz\_connect()](function.yaz-connect.md)

`type`

Строка, представляющая тип Extended Service:`itemorder`(Item Order),`create`(Create Database),`drop`(Drop Database),`commit`(Commit Operation),`update`(Update Record),`xmlupdate` (XML Update). Кожен тип вказано у наступному розділі.

`args`

Масив з Extended Service та параметрами для конкретних пакетів. Параметри ідентичні тим, що пропонуються у C API ZOOM C. Дивіться ZOOM [» Extended Services](http://www.indexdata.dk/yaz/doc/zoom.tkl)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання Record Update**

```php
<?php
$con = yaz_connect("myhost/database");
$args = array (
    "record" => "<gils><title>some title</title></gils>",
    "syntax" => "xml",
    "action" => "specialUpdate"
);
yaz_es($con, "update", $args);
yaz_wait();
$result = yaz_es_result($id);
?>
```

### Дивіться також

-   [yaz\_es\_result()](function.yaz-es-result.md) \- Перевіряє результат Extended Service
