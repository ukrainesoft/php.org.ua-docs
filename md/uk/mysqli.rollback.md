---
navigation:
  - mysqli.release-savepoint.md: '« mysqli::release\_savepoint'
  - mysqli.savepoint.md: 'mysqli::savepoint »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::rollback'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::rollback

# mysqli\_rollback

(PHP 5, PHP 7, PHP 8)

mysqli::rollback -- mysqli\_rollback - Відкат поточної транзакції

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

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

`flags`

Битовая маска констант\*\*`MYSQLI_TRANS_COR_*`\*\*

`name`

Якщо передано, то виконується `ROLLBACK/*name*/`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `name` тепер допускає значення null. |

### Приклади

Смотрите Приклад использования в разделе[](mysqli.begin-transaction.md#mysqli.begin-transaction.example.basic)[mysqli::begin\_transaction()](mysqli.begin-transaction.md)

### Примітки

> **Зауваження** :
> 
> Функція не працює з нетранзакційними типами таблиць (наприклад, MyISAM або ISAM).

### Дивіться також

-   [mysqli\_begin\_transaction()](mysqli.begin-transaction.md) \- Стартує транзакцію
-   [mysqli\_commit()](mysqli.commit.md) \- Фіксує поточну транзакцію
-   [mysqli\_autocommit()](mysqli.autocommit.md) \- Вмикає або вимикає автоматичну фіксацію змін бази даних
-   [mysqli\_release\_savepoint()](mysqli.release-savepoint.md) \- Видаляє іменовану точку збереження зі списку точок збереження поточної транзакції
