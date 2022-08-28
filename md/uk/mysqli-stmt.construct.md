Конструктор для об'єкту mysqlistmt

-   [« mysqli\_stmt::close](mysqli-stmt.close.html)
    
-   [mysqli\_stmt::data\_seek »](mysqli-stmt.data-seek.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli\_stmt](class.mysqli-stmt.html)
    
-   Конструктор для об'єкту mysqlistmt
    

# mysqlistmt::construct

(PHP 5, PHP 7, PHP 8)

mysqlistmt::construct — Конструктор для об'єкту [mysqli\_stmt](class.mysqli-stmt.html)

### Опис

public **mysqlistmt::construct**[mysqli](class.mysqli.html) `$mysql`, ?string `$query` **`null`**

Цей метод створює новий об'єкт класу [mysqli\_stmt](class.mysqli-stmt.html)

### Список параметрів

`link`

Коректний об'єкт [mysqli](class.mysqli.html)

`query`

Рядок, що містить SQL-запит. Якщо цей параметр **`null`**, то результат буде аналогічним виклику [mysqli\_stmt\_init()](mysqli.stmt-init.html), інакше результат буде аналогічний виклику [mysqli\_prepare()](mysqli.prepare.html)

### список змін

| Версия | Описание |
| --- | --- |
|  | `query` тепер допускає значення null. |

### Дивіться також

-   [mysqli\_prepare()](mysqli.prepare.html) - готує SQL вираз до виконання
-   [mysqli\_stmt\_init()](mysqli.stmt-init.html) - Ініціалізує запит та повертає об'єкт для використання у mysqlistmtprepare