---
navigation:
  - function.yaz-ccl-conf.md: « yazcclconf
  - function.yaz-close.md: yazclose »
  - index.md: PHP Manual
  - ref.yaz.md: Функции YAZ
title: yazcclparse
---
# yazcclparse

(PHP 4> = 4.0.5, PECL yaz> = 0.9.0)

yazcclparse — Викликає парсер CCL

### Опис

```methodsynopsis
yaz_ccl_parse(resource $id, string $query, array &$result): bool
```

Функція викликає синтаксичний аналізатор CCL. Він перетворює цей запит CCL FIND на запит RPN, який можна передати функції [yazsearch()](function.yaz-search.md) для пошуку.

Щоб визначити набір допустимих полів CCL, викличте [yazcclconf()](function.yaz-ccl-conf.md) перед цією функцією.

### Список параметрів

`id`

Ресурс з'єднання, повернутий [yazconnect()](function.yaz-connect.md)

`query`

Запит CCL FIND.

`result`

Якщо функцію було виконано успішно, це буде масив, що містить коректний запит RPN у ключі `rpn`

Після збою в цьому масиві встановлюються три індекси, що вказують на причину виникнення помилки:

-   `errorcode` - код помилки CCL (ціле число)
    
-   `errorstring` - Рядок помилки CCL
    
-   `errorpos` - приблизна позиція у запиті помилки (ціле число – позиція символу)
    

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Розбір CCL**

Ми спробуємо пошукати за допомогою CCL. У наведеному нижче прикладі `$ccl` є запитом CCL.

```php
<?php

yaz_ccl_conf($id, $fields);  // смотрите пример для yaz_ccl_conf
if (!yaz_ccl_parse($id, $ccl, &$cclresult)) {
    echo 'Ошибка: ' . $cclresult["errorstring"];
} else {
    $rpn = $cclresult["rpn"];
    yaz_search($id, "rpn", $rpn);
}
?>
```
