Конструктор для об'єкту mysqlistmt

-   [« mysqlistmt::close](mysqli-stmt.close.html)
    
-   [mysqlistmt::dataseek »](mysqli-stmt.data-seek.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlistmt](class.mysqli-stmt.html)
    
-   Конструктор для об'єкту mysqlistmt
    

# mysqlistmt::construct

(PHP 5, PHP 7, PHP 8)

mysqlistmt::construct — Конструктор для об'єкту [mysqlistmt](class.mysqli-stmt.html)

### Опис

public **mysqlistmt::construct**[mysqli](class.mysqli.html) `$mysql`, ?string `$query` **`null`**

Цей метод створює новий об'єкт класу [mysqlistmt](class.mysqli-stmt.html)

### Список параметрів

`link`

Коректний об'єкт [mysqli](class.mysqli.html)

`query`

Рядок, що містить SQL-запит. Якщо цей параметр **`null`**, то результат буде аналогічним виклику [mysqlistmtinit()](mysqli.stmt-init.html), інакше результат буде аналогічний виклику [mysqliprepare()](mysqli.prepare.html)

### список змін

| Версия | Описание                              |
|--------|---------------------------------------|
|        | `query` тепер допускає значення null. |

### Дивіться також

-   [mysqliprepare()](mysqli.prepare.html) - готує SQL вираз до виконання
-   [mysqlistmtinit()](mysqli.stmt-init.html) - Ініціалізує запит та повертає об'єкт для використання у mysqlistmtprepare