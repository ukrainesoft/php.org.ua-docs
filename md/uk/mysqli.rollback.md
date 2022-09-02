---
navigation:
  - mysqli.release-savepoint.md: '« mysqli::releasesavepoint'
  - mysqli.savepoint.md: 'mysqli::savepoint »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
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

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.md) або [mysqliinit()](mysqli.init.md)

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

Дивіться приклад використання у розділі [](mysqli.begin-transaction.md#mysqli.begin-transaction.example.basic)[mysqli::begintransaction()](mysqli.begin-transaction.md)

### Примітки

> **Зауваження**
> 
> Функція не працює з нетранзакційними типами таблиць (наприклад, MyISAM або ISAM).

### Дивіться також

-   [mysqlibegintransaction()](mysqli.begin-transaction.md) - Стартує транзакцію
-   [mysqlicommit()](mysqli.commit.md) - Фіксує поточну транзакцію
-   [mysqliautocommit()](mysqli.autocommit.md) - Вмикає або вимикає автоматичну фіксацію змін бази даних
-   [mysqlireleasesavepoint()](mysqli.release-savepoint.md) - Видаляє іменовану точку збереження зі списку точок збереження поточної транзакції
