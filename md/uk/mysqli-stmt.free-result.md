Звільняє пам'ять від результату запиту, вказаного дескриптором

-   [« mysqli\_stmt::$field\_count](mysqli-stmt.field-count.html)
    
-   [mysqli\_stmt::get\_result »](mysqli-stmt.get-result.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli\_stmt](class.mysqli-stmt.html)
    
-   Звільняє пам'ять від результату запиту, вказаного дескриптором
    

# mysqlistmt::freeresult

# mysqlistmtfreeresult

(PHP 5, PHP 7, PHP 8)

mysqlistmt::freeresult -- mysqlistmtfreeresult — Звільняє пам'ять від результату запиту, вказаного дескриптором

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::free_result(): void
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_free_result(mysqli_stmt $statement): void
```

Звільняє від результату запиту пам'ять, яка була зарезервована за допомогою [mysqli\_stmt\_store\_result()](mysqli-stmt.store-result.html)

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.html), отриманий за допомогою [mysqli\_stmt\_init()](mysqli.stmt-init.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [mysqli\_stmt\_store\_result()](mysqli-stmt.store-result.html) - Зберігає набір результатів у внутрішньому буфері