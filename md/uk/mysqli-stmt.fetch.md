---
navigation:
  - mysqli-stmt.execute.md: '« mysqli\_stmt::execute'
  - mysqli-stmt.field-count.md: 'mysqli\_stmt::$field\_count »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::fetch'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::fetch

# mysqli\_stmt\_fetch

(PHP 5, PHP 7, PHP 8)

mysqli\_stmt::fetch -- mysqli\_stmt\_fetch - пов'язує результати підготовленого виразу зі змінними

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::fetch(): ?bool
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_fetch(mysqli_stmt $statement): ?bool
```

Зв'язує результати підготовленого виразу зі змінними, визначеними за допомогою [mysqli\_stmt\_bind\_result()](mysqli-stmt.bind-result.md)

> **Зауваження** :
> 
> Необхідно відзначити, що всі стовпці повинні бути пов'язані перед викликом **mysqli\_stmt\_fetch()**

> **Зауваження** :
> 
> Дані не буферизуються під час передачі, коли викликається [mysqli\_stmt\_store\_result()](mysqli-stmt.store-result.md)що знижує продуктивність (але також знижує витрати пам'яті).

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

### Значення, що повертаються

**Значення, що повертаються**

| Значение | Опис |
| --- | --- |
| **`true`** | Успіх. Дані були обрані |
| **`false`** | Виникла помилка |
| **`null`** | Більше немає рядків/даних або відбулося усічення даних |

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* Проверить соединение */
if (mysqli_connect_errno()) {
    printf("Попытка соединения не удалась: %s\n", mysqli_connect_error());
    exit();
}

$query = "SELECT Name, CountryCode FROM City ORDER by ID DESC LIMIT 150,5";

if ($stmt = $mysqli->prepare($query)) {

    /* Запустить выражение */
    $stmt->execute();

    /* Определить переменные для результата */
    $stmt->bind_result($name, $code);

    /* Выбрать значения */
    while ($stmt->fetch()) {
        printf ("%s (%s)\n", $name, $code);
    }

    /* Завершить запрос */
    $stmt->close();
}

/* Закрыть соединение */
$mysqli->close();
?>
```

**Приклад #2 Процедурний стиль**

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* Проверить соединение */
if (mysqli_connect_errno()) {
    printf("Попытка соединения не удалась: %s\n", mysqli_connect_error());
    exit();
}

$query = "SELECT Name, CountryCode FROM City ORDER by ID DESC LIMIT 150,5";

if ($stmt = mysqli_prepare($link, $query)) {

    /* Запустить запрос */
    mysqli_stmt_execute($stmt);

    /* Определить переменные для результата */
    mysqli_stmt_bind_result($stmt, $name, $code);

    /* Выбрать значения */
    while (mysqli_stmt_fetch($stmt)) {
        printf ("%s (%s)\n", $name, $code);
    }

    /* Завершить запрос */
    mysqli_stmt_close($stmt);
}

/* Закрыть соединение */
mysqli_close($link);
?>
```

Результат виконання наведених прикладів:

```
Rockford (USA)
Tallahassee (USA)
Salinas (USA)
Santa Clarita (USA)
Springfield (USA)
```

### Дивіться також

-   [mysqli\_prepare()](mysqli.prepare.md) \- готує SQL вираз до виконання
-   [mysqli\_stmt\_errno()](mysqli-stmt.errno.md) \- Повертає код помилки виконання останнього запиту
-   [mysqli\_stmt\_error()](mysqli-stmt.error.md) \- Повертає рядок із поясненням останньої помилки під час виконання запиту
-   [mysqli\_stmt\_bind\_result()](mysqli-stmt.bind-result.md) \- Прив'язка змінних до підготовленого запиту для розміщення результату
