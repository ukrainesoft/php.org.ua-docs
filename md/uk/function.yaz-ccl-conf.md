---
navigation:
  - function.yaz-addinfo.md: « yaz\_addinfo
  - function.yaz-ccl-parse.md: yaz\_ccl\_parse »
  - index.md: PHP Manual
  - ref.yaz.md: Функції YAZ
title: yaz\_ccl\_conf
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# yaz\_ccl\_conf

(PHP 4 >= 4.0.5, PECL yaz >= 0.9.0)

yaz\_ccl\_conf — Конфігурує CCL-парсер

### Опис

```methodsynopsis
yaz_ccl_conf(resource $id, array $config): void
```

Функція конфігурує CCL-парсер запитів для сервера з визначеннями точок доступу (CCL-кваліфікаторів) та їх відображення у RPN.

Для відображення специфічного CCL-запиту до RPN викличте функцію [yaz\_ccl\_parse()](function.yaz-ccl-parse.md)

### Список параметрів

`id`

Ідентифікатор ресурсу, що повертається функцією [yaz\_connect()](function.yaz-connect.md)

`config`

Масив налаштувань. Кожен ключ масиву - це ім'я CCL-поля та відповідне значення, що містить рядок, який визначає відображення RPN.

Відображення – це послідовність пар атрибут-тип, атрибут-значення. Атрибут-тип та атрибут-значення розділені знаком рівності (`=`). Кожна пара відокремлюється пробілом.

Додаткову інформацію можна знайти на сторінці [» CCL](http://www.indexdata.dk/yaz/doc/tools.tkl#CCL)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

У прикладі CCL-парсер налаштований для підтримки трьох полів CCL: `ti` `au`и`isbn`. Кожне поле відображається у його BIB-1 еквіваленті. Вважається, що змінна `$id` - Це цільовий ID.

**Приклад #1 Налаштування CCL**

```php
<?php
$fields = array(
  "ti" => "1=4",
  "au"   => "1=1",
  "isbn" => "1=7"
);
yaz_ccl_conf($id, $fields);
?>
```

### Дивіться також

-   [yaz\_ccl\_parse()](function.yaz-ccl-parse.md) \- Викликає парсер CCL
