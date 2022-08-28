Викликає парсер CCL

-   [« yaz\_ccl\_conf](function.yaz-ccl-conf.html)
    
-   [yaz\_close »](function.yaz-close.html)
    
-   [PHP Manual](index.html)
    
-   [Функции YAZ](ref.yaz.html)
    
-   Викликає парсер CCL
    

# yazcclparse

(PHP 4> = 4.0.5, PECL yaz> = 0.9.0)

yazcclparse — Викликає парсер CCL

### Опис

```methodsynopsis
yaz_ccl_parse(resource $id, string $query, array &$result): bool
```

Функція викликає синтаксичний аналізатор CCL. Він перетворює цей запит CCL FIND на запит RPN, який можна передати функції [yaz\_search()](function.yaz-search.html) для пошуку.

Щоб визначити набір допустимих полів CCL, викличте [yaz\_ccl\_conf()](function.yaz-ccl-conf.html) перед цією функцією.

### Список параметрів

`id`

Ресурс з'єднання, повернутий [yaz\_connect()](function.yaz-connect.html)

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