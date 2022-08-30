Вказує ім'я набору елементів для пошуку

-   [« yazdatabase](function.yaz-database.html)
    
-   [yazerrno »](function.yaz-errno.html)
    
-   [PHP Manual](index.html)
    
-   [Функции YAZ](ref.yaz.html)
    
-   Вказує ім'я набору елементів для пошуку
    

# yazelement

(PHP 4> = 4.0.1, PECL yaz> = 0.9.0)

yazelement — Вказує ім'я набору елементів для пошуку

### Опис

```methodsynopsis
yaz_element(resource $id, string $elementset): bool
```

Функція встановлює ім'я набору елементів пошуку.

Викличте цю функцію перед [yazsearch()](function.yaz-search.html) або [yazpresent()](function.yaz-present.html), щоб вказати ім'я набору елементів для записів, що виймаються.

> **Зауваження**
> 
> Якщо здається, що не відбувається жодного ефекту, дивіться опис опції `piggybacking` в [yazconnect()](function.yaz-connect.html)

### Список параметрів

`id`

Ресурс з'єднання, повернутий [yazconnect()](function.yaz-connect.html)

`elementset`

Більшість серверів підтримують `F` (для повних записів) та `B` (Для коротких записів).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.