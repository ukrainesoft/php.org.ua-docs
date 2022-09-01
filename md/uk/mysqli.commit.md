---
navigation:
  - mysqli.close.html: '« mysqli::close'
  - mysqli.connect-errno.html: 'mysqli::$connecterrno »'
  - index.html: PHP Manual
  - class.mysqli.html: mysqli
title: 'mysqli::commit'
---
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

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.md)

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

Дивіться приклад використання у розділі [](mysqli.begin-transaction.html#mysqli.begin-transaction.example.basic)[mysqli::begintransaction()](mysqli.begin-transaction.md)

### Примітки

> **Зауваження**
> 
> Функція не працює з нетранзакційними типами таблиць (наприклад, MyISAM або ISAM).

### Дивіться також

-   [mysqliautocommit()](mysqli.autocommit.md) - Вмикає або вимикає автоматичну фіксацію змін бази даних
-   [mysqlibegintransaction()](mysqli.begin-transaction.md) - Стартує транзакцію
-   [mysqlirollback()](mysqli.rollback.md) - Відкат поточної транзакції
-   [mysqlisavepoint()](mysqli.savepoint.md) - Встановіть іменовану точку збереження транзакції
