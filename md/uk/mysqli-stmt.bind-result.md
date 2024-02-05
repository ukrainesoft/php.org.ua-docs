---
navigation:
  - mysqli-stmt.bind-param.md: '« mysqli\_stmt::bind\_param'
  - mysqli-stmt.close.md: 'mysqli\_stmt::close »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::bind\_result'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::bind\_result

# mysqli\_stmt\_bind\_result

(PHP 5, PHP 7, PHP 8)

mysqli\_stmt::bind\_result -- mysqli\_stmt\_bind\_result — Прив'язка змінних до підготовленого запиту для розміщення результату

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::bind_result(mixed &$var, mixed &...$vars): bool
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_bind_result(mysqli_stmt $statement, mixed &$var, mixed &...$vars): bool
```

Прив'язує стовпці результуючого набору змінних.

При виклику [mysqli\_stmt\_fetch()](mysqli-stmt.fetch.md) для вибірки даних, протокол клієнт-серверної взаємодії MySQL поміщає вибрані дані у змінні `var` `vars`, прив'язані до стовпців результату вибірки.

Стовпці можна прив'язувати та перев'язувати багаторазово, навіть коли результуючий набір вже частково вибраний. Нова прив'язка дасть ефект при наступному виклику [mysqli\_stmt\_fetch()](mysqli-stmt.fetch.md)

> **Зауваження** :
> 
> Усі стовпці повинні бути прив'язані до змінних після виклику [mysqli\_stmt\_execute()](mysqli-stmt.execute.md) та до виклику [mysqli\_stmt\_fetch()](mysqli-stmt.fetch.md). Залежно від типів даних стовпців прив'язані змінні можуть змінювати свій PHP тип.

> **Зауваження** :
> 
> Залежно від типів стовпців пов'язані змінні можуть змінюватися непомітно на відповідний тип PHP.

**Підказка**

Функція корисна для найпростіших результатів. Щоб отримати повторюваний набір результатів або кожний рядок як масив чи об'єкт, використовуйте [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.md)

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

`var`

Змінна, що прив'язується.

`vars`

Інші змінні, що прив'язуються.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* подготовка запроса */
$stmt = $mysqli->prepare("SELECT Code, Name FROM Country ORDER BY Name LIMIT 5");
$stmt->execute();

/* привязка переменных к подготовленному запросу */
$stmt->bind_result($col1, $col2);

/* получение значений */
while ($stmt->fetch()) {
    printf("%s %s\n", $col1, $col2);
}
```

**Приклад #2 Процедурний стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* подготовка запроса */
$stmt = mysqli_prepare($link, "SELECT Code, Name FROM Country ORDER BY Name LIMIT 5");
mysqli_stmt_execute($stmt);

/* привязка переменных к подготовленному запросу */
mysqli_stmt_bind_result($stmt, $col1, $col2);

/* получение значений */
while (mysqli_stmt_fetch($stmt)) {
    printf("%s %s\n", $col1, $col2);
}
```

Результат виконання наведених прикладів:

```
AFG Afghanistan
ALB Albania
DZA Algeria
ASM American Samoa
AND Andorra
```

### Дивіться також

-   [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.md) \- Отримує результат із підготовленого запиту у вигляді об'єкта mysqli\_result
-   [mysqli\_stmt\_bind\_param()](mysqli-stmt.bind-param.md) \- Прив'язка змінних до параметрів запиту, що готується.
-   [mysqli\_stmt\_execute()](mysqli-stmt.execute.md) \- Виконує підготовлене затвердження
-   [mysqli\_stmt\_fetch()](mysqli-stmt.fetch.md) \- пов'язує результати підготовленого виразу зі змінними
-   [mysqli\_prepare()](mysqli.prepare.md) \- готує SQL вираз до виконання
-   [mysqli\_stmt\_prepare()](mysqli-stmt.prepare.md) \- готує затвердження SQL до виконання
