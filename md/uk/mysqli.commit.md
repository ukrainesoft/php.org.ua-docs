Фіксує поточну транзакцію

-   [« mysqli::close](mysqli.close.html)
    
-   [mysqli::$connect\_errno »](mysqli.connect-errno.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Фіксує поточну транзакцію
    

# mysqli::commit

# mysqlicommit

(PHP 5, PHP 7, PHP 8)

mysqli::commit -- mysqlicommit - Фіксує поточну транзакцію

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::commit(int $flags = 0, ?string $name = null): bool
```

Процедурний стиль

```methodsynopsis
mysqli_commit(mysqli $mysql, int $flags = 0, ?string $name = null): bool
```

Фіксує транзакцію для з'єднання з базою даних.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqli\_connect()](function.mysqli-connect.html) або [mysqli\_init()](mysqli.init.html)

`flags`

Бітмаска констант **`MYSQLI_TRANS_COR_*`**

`name`

Якщо передано, то виконується `COMMIT/*name*/`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `name` тепер допускає значення null. |

### Приклади

Дивіться приклад використання у розділі [](mysqli.begin-transaction.html#mysqli.begin-transaction.example.basic)[mysqli::begin\_transaction()](mysqli.begin-transaction.html)

### Примітки

> **Зауваження**
> 
> Функція не працює з нетранзакційними типами таблиць (наприклад, MyISAM або ISAM).

### Дивіться також

-   [mysqli\_autocommit()](mysqli.autocommit.html) - Вмикає або вимикає автоматичну фіксацію змін бази даних
-   [mysqli\_begin\_transaction()](mysqli.begin-transaction.html) - Стартує транзакцію
-   [mysqli\_rollback()](mysqli.rollback.html) - Відкат поточної транзакції
-   [mysqli\_savepoint()](mysqli.savepoint.html) - Встановіть іменовану точку збереження транзакції