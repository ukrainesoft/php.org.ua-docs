Прив'язка змінних до підготовленого запиту для розміщення результату

-   [« mysqli\_stmt::bind\_param](mysqli-stmt.bind-param.html)
    
-   [mysqli\_stmt::close »](mysqli-stmt.close.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli\_stmt](class.mysqli-stmt.html)
    
-   Прив'язка змінних до підготовленого запиту для розміщення результату
    

# mysqlistmt::bindresult

# mysqlistmtbindresult

(PHP 5, PHP 7, PHP 8)

mysqlistmt::bindresult -- mysqlistmtbindresult — Прив'язка змінних до підготовленого запиту для розміщення результату

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

При виклику [mysqli\_stmt\_fetch()](mysqli-stmt.fetch.html) для вибірки даних, протокол клієнт-серверної взаємодії MySQL поміщає вибрані дані у змінні `var``vars`, прив'язані до стовпців результату вибірки.

Стовпці можна прив'язувати та перев'язувати багаторазово, навіть коли результуючий набір вже частково вибраний. Нова прив'язка дасть ефект при наступному виклику [mysqli\_stmt\_fetch()](mysqli-stmt.fetch.html)

> **Зауваження**
> 
> Усі стовпці повинні бути прив'язані до змінних після виклику [mysqli\_stmt\_execute()](mysqli-stmt.execute.html) та до виклику [mysqli\_stmt\_fetch()](mysqli-stmt.fetch.html). Залежно від типів даних стовпців прив'язані змінні можуть змінювати свій PHP тип.

> **Зауваження**
> 
> Залежно від типів стовпців пов'язані змінні можуть змінюватися непомітно на відповідний тип PHP.

**Підказка**

Функція корисна для найпростіших результатів. Щоб отримати повторюваний набір результатів або кожний рядок як масив чи об'єкт, використовуйте [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.html)

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.html), отриманий за допомогою [mysqli\_stmt\_init()](mysqli.stmt-init.html)

`var`

Змінна, що прив'язується.

`vars`

Інші змінні, що прив'язуються.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* подготовка запроса */
$stmt = $mysqli->prepare("SELECT Code, Name FROM Country ORDER BY Name LIMIT 5");
$stmt->execute();

/* привязка переменных к подготовленному запросу */
$stmt->bind_result($col1, $col2);

/* получение значений */
while ($stmt->fetch()) {
    printf("%s %s\n", $col1, $col2);
}
```

**Приклад #2 Процедурний стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* подготовка запроса */
$stmt = mysqli_prepare($link, "SELECT Code, Name FROM Country ORDER BY Name LIMIT 5");
mysqli_stmt_execute($stmt);

/* привязка переменных к подготовленному запросу */
mysqli_stmt_bind_result($stmt, $col1, $col2);

/* получение значений */
while (mysqli_stmt_fetch($stmt)) {
    printf("%s %s\n", $col1, $col2);
}
```

Результат виконання даних прикладів:

```
AFG Afghanistan
ALB Albania
DZA Algeria
ASM American Samoa
AND Andorra
```

### Дивіться також

-   [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.html) - Отримує результат із підготовленого запиту у вигляді об'єкта mysqliresult
-   [mysqli\_stmt\_bind\_param()](mysqli-stmt.bind-param.html) - Прив'язка змінних до параметрів запиту, що готується.
-   [mysqli\_stmt\_execute()](mysqli-stmt.execute.html) - Виконує підготовлене затвердження
-   [mysqli\_stmt\_fetch()](mysqli-stmt.fetch.html) - пов'язує результати підготовленого виразу зі змінними
-   [mysqli\_prepare()](mysqli.prepare.html) - готує SQL вираз до виконання
-   [mysqli\_stmt\_prepare()](mysqli-stmt.prepare.html) - готує затвердження SQL до виконання