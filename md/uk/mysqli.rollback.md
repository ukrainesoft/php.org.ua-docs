Відкат поточної транзакції

-   [« mysqli::release\_savepoint](mysqli.release-savepoint.html)
    
-   [mysqli::savepoint »](mysqli.savepoint.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Відкат поточної транзакції
    

# mysqli::rollback

# mysqlirollback

(PHP 5, PHP 7, PHP 8)

mysqli::rollback -- mysqlirollback - Відкат поточної транзакції

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::rollback(int $flags = 0, ?string $name = null): bool
```

Процедурний стиль

```methodsynopsis
mysqli_rollback(mysqli $mysql, int $flags = 0, ?string $name = null): bool
```

Відкочує поточну транзакцію.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqli\_connect()](function.mysqli-connect.html) або [mysqli\_init()](mysqli.init.html)

`flags`

Бітова маска констант **`MYSQLI_TRANS_COR_*`**

`name`

Якщо передано, то виконується `ROLLBACK/*name*/`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                             |
|--------|--------------------------------------|
|        | `name` тепер допускає значення null. |

### Приклади

Дивіться приклад використання у розділі [](mysqli.begin-transaction.html#mysqli.begin-transaction.example.basic)[mysqli::begin\_transaction()](mysqli.begin-transaction.html)

### Примітки

> **Зауваження**
> 
> Функція не працює з нетранзакційними типами таблиць (наприклад, MyISAM або ISAM).

### Дивіться також

-   [mysqli\_begin\_transaction()](mysqli.begin-transaction.html) - Стартує транзакцію
-   [mysqli\_commit()](mysqli.commit.html) - Фіксує поточну транзакцію
-   [mysqli\_autocommit()](mysqli.autocommit.html) - Вмикає або вимикає автоматичну фіксацію змін бази даних
-   [mysqli\_release\_savepoint()](mysqli.release-savepoint.html) - Видаляє іменовану точку збереження зі списку точок збереження поточної транзакції