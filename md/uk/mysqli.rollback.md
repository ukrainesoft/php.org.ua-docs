---
navigation:
  - mysqli.release-savepoint.html: '« mysqli::releasesavepoint'
  - mysqli.savepoint.html: 'mysqli::savepoint »'
  - index.html: PHP Manual
  - class.mysqli.html: mysqli
title: 'mysqli::rollback'
---
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

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.html)

`flags`

Бітова маска констант **`MYSQLI_TRANS_COR_*`**

`name`

Якщо передано, то виконується `ROLLBACK/*name*/`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `name` тепер допускає значення null. |

### Приклади

Дивіться приклад використання у розділі [](mysqli.begin-transaction.html#mysqli.begin-transaction.example.basic)[mysqli::begintransaction()](mysqli.begin-transaction.html)

### Примітки

> **Зауваження**
> 
> Функція не працює з нетранзакційними типами таблиць (наприклад, MyISAM або ISAM).

### Дивіться також

-   [mysqlibegintransaction()](mysqli.begin-transaction.html) - Стартує транзакцію
-   [mysqlicommit()](mysqli.commit.html) - Фіксує поточну транзакцію
-   [mysqliautocommit()](mysqli.autocommit.html) - Вмикає або вимикає автоматичну фіксацію змін бази даних
-   [mysqlireleasesavepoint()](mysqli.release-savepoint.html) - Видаляє іменовану точку збереження зі списку точок збереження поточної транзакції
