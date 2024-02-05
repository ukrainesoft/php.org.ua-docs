---
navigation:
  - mysqli.begin-transaction.md: '« mysqli::begin\_transaction'
  - mysqli.character-set-name.md: 'mysqli::character\_set\_name »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::change\_user'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::change\_user

# mysqli\_change\_user

(PHP 5, PHP 7, PHP 8)

mysqli::change\_user -- mysqli\_change\_user — Дозволяє змінити користувача підключеного до бази даних

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::change_user(string $username, string $password, ?string $database): bool
```

Процедурний стиль

```methodsynopsis
mysqli_change_user(    mysqli $mysql,    string $username,    string $password,    ?string $database): bool
```

Змінює користувача, від імені якого здійснено підключення до бази даних, та встановлює поточну базу даних

Для успішної зміни користувача необхідні коректні `username`и`password`а також наявність достатніх прав для роботи з базою. Якщо зміна користувача закінчиться помилкою, збережеться поточна авторизація користувача до виклику функції.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

`username`

Ім'я користувача для доступу до MySQL

`password`

Пароль для доступу до MySQL

`database`

Ім'я бази даних

Якщо потрібно змінити користувача без вибору бази даних, слід вказувати **`null`**. Для вибору бази даних необхідно використовувати функцію [mysqli\_select\_db()](mysqli.select-db.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### Приклади

**Пример #1 Пример использования**mysqli::change\_user()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php

/* создаём подключение к базе данных test */
$mysqli = new mysqli("localhost", "my_user", "my_password", "test");

/* проверяем соединение */
if (mysqli_connect_errno()) {
    printf("Подключение не удалось: %s\n", mysqli_connect_error());
    exit();
}

/* устанавливаем переменную a */
$mysqli->query("SET @a:=1");

/* все сбрасываем и выбираем новую базу данных */
$mysqli->change_user("my_user", "my_password", "world");

if ($result = $mysqli->query("SELECT DATABASE()")) {
    $row = $result->fetch_row();
    printf("База данных по умолчанию: %s\n", $row[0]);
    $result->close();
}

if ($result = $mysqli->query("SELECT @a")) {
    $row = $result->fetch_row();
    if ($row[0] === NULL) {
        printf("Значение переменной - NULL\n");
    }
    $result->close();
}

/* закрываем соединение */
$mysqli->close();
?>
```

Процедурний стиль

```php
<?php
/* создаём подключение к базе данных test */
$link = mysqli_connect("localhost", "my_user", "my_password", "test");

/* проверяем соединение */
if (!$link) {
    printf("Подключение не удалось: %s\n", mysqli_connect_error());
    exit();
}

/* устанавливаем переменную a */
mysqli_query($link, "SET @a:=1");

/* все сбрасываем и выбираем новую базу данных */
mysqli_change_user($link, "my_user", "my_password", "world");

if ($result = mysqli_query($link, "SELECT DATABASE()")) {
    $row = mysqli_fetch_row($result);
    printf("База данных по умолчанию: %s\n", $row[0]);
    mysqli_free_result($result);
}

if ($result = mysqli_query($link, "SELECT @a")) {
    $row = mysqli_fetch_row($result);
    if ($row[0] === NULL) {
        printf("Значение переменной - NULL\n");
    }
    mysqli_free_result($result);
}

/* закрываем соединение */
mysqli_close($link);
?>
```

Результат виконання наведених прикладів:

```
База данных по умолчанию: world
Значение переменной - NULL
```

### Примітки

> **Зауваження** :
> 
> В результаті виклику функції поточне з'єднання з базою даних починає поводитися так, ніби було створено нове з'єднання. Незалежно від результату операції, виклик функції призводить до відкату всіх активних транзакцій, закриття часових таблиць та розблокування всіх заблокованих таблиць.

### Дивіться також

-   [mysqli\_connect()](function.mysqli-connect.md) \- Псевдонім mysqli::\_\_construct
-   [mysqli\_select\_db()](mysqli.select-db.md) \- Встановлює базу даних для запитів, що виконуються.
